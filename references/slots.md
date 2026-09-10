# The eight slots

Where the metaphor is allowed to live, and what each slot is for.

## Contents

- [Why eight](#why-eight)
- [Slot by slot](#slot-by-slot)
- [Which slots earn the most](#which-slots-earn-the-most)
- [Worked example: three metaphors across all eight](#worked-example-three-metaphors-across-all-eight)
- [Content mapping — the ninth move](#content-mapping--the-ninth-move)
- [Implementation notes](#implementation-notes)

## Why eight

Constraint is what makes this method repeatable rather than a gamble. The eight
slots are all *furniture* — the parts of a page that exist regardless of what
the page is about. Because they are structural, applying an idea to them is
felt everywhere without touching the content, so the page keeps working while
still feeling specific.

Let the metaphor spread past these and it becomes a costume: the reader starts
fighting the design to get at the information.

## Slot by slot

### 1. Header / nav — the "top" of the metaphor

Whatever the top of the object, place or process is. The lid of a laptop. The
lit sign above a shop. The surface of the water. Sky.

Keep it usable: it is still the navigation, and on a phone it is competing for
the most valuable space on the page. A concept that makes the header taller is
usually a bad trade.

### 2. Page backdrop — the base

The color or texture the whole page sits on. Where a time-of-day or depth
metaphor pays off most, because one long gradient does the work.

Long vertical gradients band visibly on cheap screens. A very low-opacity noise
overlay dithers this away for almost nothing.

### 3. Section transitions — how one section becomes the next

The highest-value slot after the backdrop, and the most often wasted. This is
where a metaphor becomes structural instead of decorative: layers of a burger,
sheets of paper overlapping, a strand of lights slung between sections, a change
in water depth.

### 4. Dividers & rules — the connective pieces

The small version of slot 3. A short strand, a torn edge, a length of measuring
tape, a keyway profile.

### 5. Scroll indicator — progress, in the metaphor's language

Cheap to build and disproportionately memorable, because it responds to the
reader. A burger assembling. Bulbs lighting up. A cup filling. A candle burning
down. A tachometer sweeping.

Make it a real progress cue, not just an animation — it should tell the reader
where they are. And it must have a genuine reduced-motion path: render the
finished state and skip the scroll listener entirely.

### 6. Buttons & hover — micro-interactions

Press states, hovers, focus rings in the same language. A filament warming. A
stamp pressing into paper. A switch throwing.

Do not sacrifice affordance for the joke. A button must still look pressable,
and focus states must stay clearly visible for keyboard users.

### 7. Footer — the "bottom", mirroring the header

The counterpart to slot 1. The bottom bun. The seabed. Sand. Full night. A
folded-over wrapper. The base of the machine.

This is also where people land when they have decided to act, so every way of
contacting the subject belongs here regardless of the metaphor.

### 8. 404 + favicon — the proof it was thought through

The tell. Anyone can theme a homepage; a themed 404 says someone cared. Keep it
useful — a way back and a way to get help — but let it carry the joke.

The favicon is the metaphor at 16 pixels: a bulb, a sticker, a key, a gauge.

## Which slots earn the most

If time is short, spend it in this order:

1. **Backdrop (2)** — sets the whole page for one decision
2. **Section transitions (3)** — turns a theme into a structure
3. **Scroll indicator (5)** — the thing people describe to other people
4. **Header + footer (1, 7)** — bookends, and they mirror each other
5. **404 + favicon (8)** — cheap, and disproportionate credit
6. **Dividers, buttons (4, 6)** — polish

## Worked example: three metaphors across all eight

| Slot | "One evening" (burger stall) | "The laptop" (IT portfolio) | "Low tide" (beach resort) |
|---|---|---|---|
| 1 Header | The lit sign off their truck | The lid, closed, opening on load | Sunlit water surface |
| 2 Backdrop | Golden hour → night gradient | Desktop wallpaper, subtly parallaxed | Turquoise → deep blue by depth |
| 3 Transitions | Strands of bulbs between sections | Each section is a different app window | Water darkening a band at a time |
| 4 Dividers | Three bulbs on a drooping wire | Window chrome, a divider rail | A tide line of wet sand |
| 5 Scroll | Bulbs lighting left to right | Battery filling / progress bar | Depth gauge descending |
| 6 Buttons | Filament glow on press | Key press with travel | Ripple outward |
| 7 Footer | Full night, bulbs brightest | The base of the machine, ports | Sand and shells |
| 8 404 | An unlit bulb, "Sold out" | A blue screen, handled gracefully | An empty rockpool |

Notice none of these needs 3D or heavy assets. The burger version was built
entirely from CSS gradients, border-radius and positioned dots.

## Content mapping — the ninth move

The eight slots are chrome. Separately, ask whether any **content type** has a
natural home inside the metaphor's object:

- Certifications → stickers on a laptop lid
- A menu → the shop's own wrapping paper
- Testimonials → postcards, if the metaphor is a place
- A process or timeline → the stages of the process the metaphor is built from
- Pricing tiers → the settings panel of the app the metaphor mimics

Go through the content types once and look for one or two of these. When a match
lands, the content stops sitting on top of the design and becomes part of it.

Force it and you get the costume problem. If a content type has no natural home,
leave it plain — most will, and that is fine.

## Implementation notes

**Weight.** A metaphor should cost kilobytes, not megabytes. Most of the ideas
above are CSS. Reach for 3D only when the concept genuinely depends on it, and
then lazy-load it below the fold behind an intersection observer with a static
fallback image. Nothing heavy above the fold.

**Dark concepts and daylight.** Atmospheric palettes look best on the laptop you
designed them on and worst on a phone outdoors. Keep whichever section carries
the critical information — prices, contact details — on a light panel regardless
of what the rest of the page is doing.

**Motion.** Under `prefers-reduced-motion: reduce`, disable rather than shorten,
and skip attaching the listeners at all. Verify it in the built output, not just
the source.

**Contrast drifts on gradients.** A backdrop that changes color down the page
will silently break text contrast somewhere in the middle. Check the actual
computed contrast at several scroll positions, not just at the top.

**Full-bleed elements and horizontal scroll.** Decorative pieces positioned at
0% and 100% of the width will push the document a few pixels wider than the
viewport. Inset them slightly and check `documentElement.scrollWidth` against
`clientWidth` at 360px, 390px and 414px.
