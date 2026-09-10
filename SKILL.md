---
name: structural-metaphor
description: Design web pages that feel built for their subject rather than assembled from a template, by deriving one structural metaphor from the subject's own artifacts and applying it consistently across the page. Use this whenever building, redesigning, or improving a website, landing page, portfolio, product page or marketing site — including existing sites and half-finished builds that need a stronger direction. Especially use it when the user wants something to "stand out", "not look like a template", "feel unique" or "have personality", asks for a creative concept, visual direction, theme or palette, says a page looks generic, boring or forgettable, or wants help working out what makes a business distinctive enough to design around. Also use when picking colours and type for a site, or when a build is drifting toward stock layout.
---

# Structural Metaphor

A method for making a page feel like it could only belong to this one subject,
without letting the creativity get in the way of what the page is for.

The core claim: a memorable page usually has **one idea**, taken from something
the subject actually owns, applied to **the page's own furniture** — the header,
the scroll, the dividers, the footer — while the layout underneath stays
completely ordinary.

Two examples of the method producing very different results:

- A burger stall in an open-air lot. The metaphor was *one evening, 5PM to
  close*: the page opened at golden hour and darkened to night as you scrolled,
  section dividers were strands of festoon bulbs, and the scroll indicator was a
  wire of bulbs lighting up left to right as you descended. It came from their
  photographs, which were all shot at dusk under string lights.
- An IT portfolio. The metaphor was *the person's laptop*: each section became a
  different app or feature of the machine, and their certifications became
  stickers on the back of the lid.

Neither is a "restaurant concept" or a "portfolio concept". Each came from the
specific subject. That is the whole point, and it is what the method protects.

## The order of work

Do not start with a mood board or a color palette. Start with an inventory.

If the site already exists — a repo, a live URL, a half-finished build — read
**[Working on a site that already exists](#working-on-a-site-that-already-exists)**
before starting. The steps below still apply, but the order changes and there are
things worth protecting.

### 1. Mine the source material before designing anything

The metaphor has to be *found*, not invented, or it reads as decoration bolted
on afterwards. Go through whatever exists and write down what you actually have:

- **Photographs.** What is physically in them? What is the light doing? What
  objects recur? Note the dominant colors — you will sample the palette from
  here rather than choosing one.
- **The subject's own words.** Bios, taglines, "about" text, social posts.
  Quote them exactly; do not paraphrase yet.
- **Physical artifacts.** Signage, packaging, wrapping paper, uniforms, tools,
  vehicles, a workspace. These are gold: they are things the subject already
  chose, so a metaphor built from them is automatically on-brand.
- **What other people say.** Reviews, testimonials, recommendations. Look for
  phrases that repeat — those are the words customers already use, so they make
  better headlines than anything you would write.
- **The friction.** Recurring complaints, or the thing that is hard about
  dealing with this subject. Design around it rather than ignoring it.

Then answer one question in a single sentence: **what is the one distinctive
concrete detail here?** Not a category trait. A specific thing. A signature
dish, the view from the second floor, the bench outside, the tool they never put
down, the line painted on the side of their van.

That detail is the seed.

**If you cannot name one, ask.** A thin inventory is not a reason to fall back
on a category cliché or to default to restraint — it usually means the
distinctive thing exists but nobody has written it down. Owners are rarely
conscious of what makes them unusual, so abstract questions ("what's your
brand?") get abstract answers. Ask for physical specifics instead:

- What do customers always comment on, even when you wish they wouldn't?
- What do you do differently from the place down the road, *even though it
  costs you more or takes longer*? (This one earns its keep most often —
  a deliberate inconvenience is nearly always the story.)
- What is the oldest thing in the building, and why is it still there?
- What would you never change, even if changing it would be easier?
- Who is your most regular customer, and what do they always order or ask for?
- What do people get wrong about you?
- What does a customer walk away holding?
- What time of day is the place most itself?

Ask three or four, not all eight. Stop as soon as something concrete and
physical comes back — that is the seed, and one good answer beats a full survey.

Only after asking, if there is genuinely nothing, design around the gap and say
so plainly rather than importing a metaphor from nowhere.

For worked examples of this step, and the common ways it goes wrong, read
`references/deriving-metaphors.md`.

### 2. Propose three concepts, and reject the obvious one out loud

**Concept A must be the predictable one for the category** — the bun-and-patty
layers for a burger place, the terminal window for a developer portfolio, the
stethoscope-and-cross for a clinic. Name it, then say plainly why you are
rejecting it: it is interchangeable, swap the logo and it fits any competitor.

Two things make this step worth the words. It proves you considered the obvious
answer rather than missing it, and it forces you to articulate what *this*
subject has that the category does not.

Occasionally Concept A is genuinely right — restraint is the correct concept for
a medical clinic, and a category-typical idea can be the strongest one when the
subject is deliberately conventional. If so, defend it rather than rejecting it
for the sake of it.

**Concepts B and C must derive from the distinctive detail**, not the category.
Two subjects in the same business should never receive the same concept.

Present each in this shape:

```
CONCEPT [A/B/C] — "[Metaphor name]"
The idea:        [one sentence]
Why this one:    [what in the source material points here]
The 8 slots:     [one line each, concrete and buildable — list is in step 3]
Palette:         [4-5 colors with hex + role, sampled from the source material]
Type:            [display face + body face, with a self-hostable fallback]
Signature move:  [the one thing people will remember]
Risk:            [where this could go gimmicky, and the mitigation]
Source fit:      [does this flatter the photos/assets that actually exist?]
```

Then **stop and let the user choose.** Do not build all three, and do not start
building your favorite. Users frequently pick a hybrid ("B, but with C's
texture"), which is usually better than any of the three alone — that only
happens if you present and pause.

### 3. Apply the metaphor to exactly eight slots

The metaphor lives in the page's furniture and nowhere else. Eight slots:

| # | Slot | What the metaphor does here |
|---|------|------------------------------|
| 1 | Header / nav | The "top" of the metaphor |
| 2 | Page backdrop | Base color or texture the page sits on |
| 3 | Section transitions | How one section becomes the next |
| 4 | Dividers & rules | The small connective pieces |
| 5 | Scroll indicator | A progress cue in the same language |
| 6 | Buttons & hover | Micro-interactions |
| 7 | Footer | The "bottom" — mirrors the header |
| 8 | 404 + favicon | The joke that proves it was thought through |

Confining it to these eight is what keeps a concept from becoming a costume.
The content areas stay plain, so the page still reads as a page.

`references/slots.md` has the slot-by-slot detail, worked examples for several
metaphors, and notes on which slots are worth the most effort.

### 4. Map the content, not just the chrome

This is the step that separates a nice theme from something people remember, and
it is the one most often skipped.

Ask: **does a content type on this page have a natural home inside the metaphor's
object?** Not the header and footer — the actual material.

- Certifications on a portfolio → stickers on the back of a laptop lid
- A menu → printed on the shop's own branded wrapping paper
- A project timeline → a filmstrip, if the subject is a photographer
- Pricing tiers → the settings panel of the app the metaphor is built from

When this lands, the content stops sitting *on* the design and starts being
*part of* it. Look for one or two of these. Do not force it onto every section —
if a content type has no natural home, leave it plain.

### 5. Take the palette and type from the source material

Sample the palette from the subject's own photographs and assets rather than
picking colors you like. When the burger stall's palette turned out to be amber,
dusk blue and red, that was not a choice — those colors were already in every
photograph, because that is what their lot looks like at 7PM. A palette derived
this way cannot clash with the photos, and it usually turns out to match the
existing brand colors, because both come from the same physical place.

Give every color a role (surface, accent, call-to-action, text) so it is obvious
where each belongs. Two type families maximum, self-hosted, with a real fallback
stack.

### 6. Keep the skeleton fixed

Section order and layout stay constant. **The skeleton is fixed; only the paint
changes.** Sections may be *renamed* to fit the metaphor, but not reordered or
dropped.

This is what makes the method reliable rather than a gamble. The parts that
determine whether a page works — hierarchy, reading order, spacing, tap targets
— are decided once and reused, so the creative energy goes somewhere it cannot
break anything.

## Working on a site that already exists

Most of the above assumes a blank page. When there is already a site — a repo,
a live URL, a half-finished build — the method still applies, but the order
changes and the risk is different: a redesign can lose things that were quietly
working.

**Inventory the existing site before the subject.** Read it as source material
in its own right. What does it already get right? Which of the eight slots is
already doing something, even accidentally? Is there a colour, a shape or a
piece of copy that is genuinely theirs and worth keeping? Sites assembled from
templates usually still contain one or two real details — a photograph the owner
insisted on, a phrase in their own voice.

**Find out what the page currently achieves before changing it.** If it ranks,
converts, or gets used a particular way, that behaviour is a constraint. Ask
before assuming a redesign is wanted at all — sometimes the honest answer is
that the layout is fine and the problem is the photography, or the copy, or a
Google listing that says "permanently closed".

**Then run the normal method**, with two adjustments:

- **Keep the skeleton that exists** unless it is genuinely broken. The point of
  a fixed skeleton is that structure is not where the creativity goes; a working
  section order is worth more than a novel one.
- **Apply the metaphor slot by slot, in the order of most leverage** (backdrop,
  section transitions, scroll indicator first). This is retrofittable
  incrementally, and it means the site improves at every step rather than
  entering a long broken middle.

Say plainly which of the eight slots you changed and which you left alone, so
the owner can see the shape of the work rather than just a new look.

## The guardrails

Creativity that breaks the page, or that lies, is worse than a plain template.
These are not bureaucratic checks — each one exists because it is the specific
way this method fails.

### The page's jobs come first

Before designing, write down the two or three things a visitor actually came to
do. For a local business it is usually: contact them, find them, see what things
cost. For a portfolio: see the work, judge whether this person is credible, get
in touch. For a product page: understand what it does, see the price, start.

**No creative decision may obstruct those.** If an idea makes the phone number
harder to find, the idea loses. Check this explicitly before building, and again
at the end.

A concrete version of this test: the concept must survive being seen on a small,
dim phone screen in daylight. Dark, atmospheric palettes are the usual casualty
— if the page goes dark, keep the section carrying the critical information on a
light panel regardless of what the rest is doing.

### Never invent a fact

Not hours, prices, dates, awards, years of experience, staff names, or
capabilities. If a fact is not in the source material, it goes in as a visible
placeholder — `TODO(owner): confirm opening hours` — styled so it is obvious on
screen and impossible to ship by accident. Collect every one into a handoff note
at the end.

This matters more than it sounds. A page that looks convincing and contains an
invented price is worse than an obviously unfinished one, because nobody catches
it before a customer does.

### Quote people verbatim

Reviews and testimonials are reproduced exactly: original spelling, punctuation,
line breaks and attribution. Do not tidy the grammar, do not shorten, do not
write new ones. Say where they came from and link to the source if there is one.

Resist marking up a subject's own testimonials as review structured data on their
own site — search engines treat self-serving review markup as ineligible for rich
results. Show them to people; do not fake them into the schema.

### Real images for real things

Photographs of the subject's actual products, spaces, people and work must be
real. Generated imagery is fine for textures, background patterns, dividers,
abstract atmosphere, icons and decorative props — the things that are obviously
ornamental.

Never generate a picture of a dish, a room, a product or a person and present it
as the subject's own. Someone will travel to that place expecting what they saw.

If a needed photo does not exist, design around the gap and write a shot list
saying exactly what to photograph, from what angle and in what light. That list
is often more valuable to the subject than another section of page.

### Motion has an off switch

Whatever the metaphor animates, `prefers-reduced-motion: reduce` must genuinely
disable it — not slow it down. If the concept has an animated scroll indicator,
under reduced motion it should render in its finished state and skip attaching
scroll listeners at all.

## Finishing

Before calling it done, walk the eight slots and confirm the metaphor is present
in each. Then check that it never obstructs the page's jobs, that it survives the
small-dim-phone test, and that the 404 and favicon carry it through — those two
are the tell for whether the concept was thought through or applied to the top of
the page and abandoned.

Two failures are near-certain whenever the concept touched the backdrop, and
neither shows up on the machine you designed it on:

- **Text contrast drifts down a gradient.** Measure the computed contrast at
  several scroll positions, not only at the top.
- **Full-bleed decoration pushes the page wider than the viewport.** Compare
  `documentElement.scrollWidth` against `clientWidth` at 360px, 390px and 414px.

Then hand over what the build could not resolve: the collected `TODO(owner)`
list, and a shot list for the photographs that do not exist yet.

State honestly which checks pass and which do not. A failed check that is
reported is useful; a failed check that is hidden is a problem handed to someone
else.
