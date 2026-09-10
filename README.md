# Structural Metaphor

A Claude skill for designing web pages that feel like they could only belong to
one subject, without letting the creativity get in the way of what the page is
for.

Most design help defaults to the *category*. Ask for a bakery site and you get a
bakery site: kraft paper, flour texture, warm cream. It isn't bad work — it's
interchangeable. Swap the logo and it fits any competitor on the same street.

This skill refuses the category. It makes the concept come from something the
subject actually owns — their photographs, their signage, the sentence painted
on the side of their van — and then confines that idea to eight fixed slots of
page furniture, so the layout underneath stays completely ordinary and keeps
working.

## The core claim

A memorable page usually has **one idea**, taken from something the subject
actually owns, applied to **the page's own furniture** — header, backdrop,
section transitions, dividers, scroll indicator, buttons, footer, 404 — while
the content areas stay plain.

Two real results from the method:

- **A burger stall in an open-air lot.** The metaphor was *one evening, 5PM to
  close*. The page opened at golden hour and darkened to night as you scrolled,
  section dividers were strands of festoon bulbs, and the scroll indicator was a
  wire of bulbs lighting up left to right as you descended. None of that was
  chosen — every photo they had was shot at dusk under string lights, so the
  palette was sampled rather than picked, and the page could not clash with the
  photographs.
- **An IT portfolio.** The metaphor was *the person's laptop*. Each section
  became a different app or feature of the machine, and their certifications
  became stickers on the back of the lid — a boring list turned into something
  instantly legible as "things this person collected".

Neither is a "restaurant concept" or a "portfolio concept."

## Installing

**Claude Code (local):**

```bash
git clone https://github.com/<you>/structural-metaphor.git ~/.claude/skills/structural-metaphor
```

Claude picks it up on the next session. To scope it to one project instead, clone
into `.claude/skills/` inside that repo.

**Claude account (web / desktop):** zip the `structural-metaphor` folder and
upload it under Settings → Capabilities → Skills. Excluding `evals/` from that
zip keeps it smaller; the skill does not read it at runtime.

## What's in here

| File | What it is |
|---|---|
| `SKILL.md` | The method. Loaded whenever the skill fires. |
| `references/deriving-metaphors.md` | Seven worked examples of getting from "here is a subject" to "here is the one idea", plus the anti-patterns. |
| `references/slots.md` | The eight slots in detail, three metaphors mapped across all of them, and implementation notes. |
| `evals/evals.json` | Three test scenarios with graded assertions. |

The two reference files are loaded on demand rather than up front, so the skill
stays cheap until it is actually doing this work.

## The method, briefly

1. **Inventory before designing.** Go through the photos, the subject's own
   words, their physical artifacts, what reviews repeat, and the friction. Write
   down what is actually there. Then name **the one distinctive concrete
   detail** — not a category trait.
2. **Propose three concepts, and reject the obvious one out loud.** Concept A
   must be the predictable category answer, named and then rejected as
   interchangeable. B and C derive from the distinctive detail. Then stop and let
   the user choose.
3. **Apply the metaphor to exactly eight slots** — and nowhere else. That
   constraint is what stops a concept becoming a costume.
4. **Map the content, not just the chrome.** Ask whether any content type has a
   natural home inside the metaphor's object. One or two will. Those are the
   ones people remember.
5. **Take the palette and type from the source material** rather than choosing
   colours you like.
6. **Keep the skeleton fixed.** Sections may be renamed to fit the metaphor,
   never reordered or dropped.

There is a separate path for sites that already exist, where the order changes
and the priority is not losing what was quietly working.

## The guardrails

Creativity that breaks the page, or that lies, is worse than a plain template.
Each of these exists because it is a specific way this method fails.

- **The page's jobs come first.** Write down the two or three things a visitor
  came to do. If an idea makes the phone number harder to find, the idea loses.
- **Never invent a fact.** Not hours, prices, dates, awards, or years of
  experience. Anything missing becomes a visible `TODO(owner)` marker, collected
  into a handoff note. A page that looks finished and contains a made-up price is
  worse than an obviously unfinished one.
- **Quote people verbatim.** Reviews keep their original spelling and
  punctuation. No tidying, no writing new ones, and no self-serving review markup
  in the schema.
- **Real images for real things.** Generated imagery is for textures and
  ornament. Never a dish, a room, a product or a person presented as the
  subject's own — someone will travel to that place expecting what they saw. If a
  needed photo doesn't exist, design around the gap and write a shot list.
- **Motion has an off switch.** `prefers-reduced-motion: reduce` must genuinely
  disable, not shorten.

## Does it work?

Tested across three scenarios, each run twice — once with the skill and once
without — with both arms building real pages rather than one arm only describing
one. Graded against assertions written before the runs.

- **28/28 assertions passed with the skill, 15/28 without.**
- The finding that replicated most reliably was **placeholder discipline**:
  **33–41 visible `TODO(owner)` markers per page with the skill, versus 0–5
  without.** Unknown facts otherwise get quietly filled in with plausible ones.

Honest limitations: three scenarios is a small sample, the grading was done by
the same author who wrote the skill, and every test was a greenfield build. The
existing-site path and the interview questions are reasoned, not measured.

## A note on the examples

Of the seven worked examples in `references/deriving-metaphors.md`, **two are
real projects** — the burger stall and the IT portfolio. The SaaS tool, the
fitness studio, the funeral home and the bespoke tailor are **constructed**,
written to cover situations the real ones didn't: an intangible product, a
category with an overwhelming cliché, a subject where restraint is the right
answer, and one so rich in artifacts that the risk is using all of them.

They are teaching examples, not a client list. The skill's own first rule is
never invent a fact, and that applies here too.

## When not to use it

If the honest answer is that the layout is fine and the real problem is the
photography, the copy, or a Google listing that says "permanently closed", this
skill should tell you that instead of redesigning something that already worked.

## License

MIT.
