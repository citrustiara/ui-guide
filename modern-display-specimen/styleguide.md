# Modern Display Specimen Styleguide

## 1. Style Character

This style turns a type specimen poster into a UI and presentation system. It uses massive compressed word rows, thin table rules, tiny metadata labels, hard-edged rectangular cells, and a limited industrial palette.

It should feel:

- editorial and mechanical,
- precise, not friendly,
- loud through scale, not decoration,
- more like a printed specimen sheet than a SaaS template,
- disciplined enough for portfolios, landing pages, and pitch slides.

Use it for portfolio covers, typographic campaign pages, visual identity decks, creative studio pages, poster-like product launches, and presentation section breaks. Avoid it for long-form dashboards, dense admin tools, or any interface where quiet repetition matters more than visual impact.

## 2. Palette

The reference image uses a very aggressive neon green. This system replaces it with oxidized rust and pearl so it keeps the punch but feels more premium and usable.

| Token | Hex | Role |
|---|---:|---|
| `--ds-pearl` | `#F4EFE5` | primary background, large calm field |
| `--ds-pearl-soft` | `#FBF7EF` | secondary paper surface |
| `--ds-rust` | `#A94732` | main specimen field and active accent |
| `--ds-rust-deep` | `#75271F` | deep hover, emphasis, dark accent blocks |
| `--ds-ink` | `#11110F` | type, rules, primary UI |
| `--ds-silver` | `#C9C6BD` | secondary cells and muted panels |
| `--ds-silver-dark` | `#8F8B82` | captions and quiet dividers |
| `--ds-muted` | `#625D54` | body copy |

Recommended proportions:

- 45-65% pearl,
- 20-35% rust,
- 10-20% black ink typography and rules,
- 5-10% silver support fields.

Do not introduce gradients, bright greens, neon colors, glass effects, or soft pastel expansions. If a chart needs extra colors, use rust tints and black/silver line patterns before adding new hues.

## 3. Typography

Recommended CSS stack:

```css
font-family: "Archivo Black", "Arial Black", "Impact", sans-serif;
```

For body and UI:

```css
font-family: "Archivo", "Aptos", "Helvetica Neue", Arial, sans-serif;
```

For metadata:

```css
font-family: "IBM Plex Mono", "Courier New", monospace;
```

Hierarchy:

| Element | Size | Weight | Case | Notes |
|---|---:|---:|---|---|
| Poster word | 90-220px | 900 | uppercase | sits in ruled rows |
| Slide title | 64-140px | 900 | uppercase | short, compressed, direct |
| Section title | 36-64px | 900 | uppercase | aligned to cells |
| Accent line | 24-42px | 900 | sentence or uppercase | can be rust on pearl |
| Body | 15-18px | 500 | sentence case | never set long paragraphs all caps |
| Metadata | 10-12px | 700 | uppercase | mono, tight, functional |

Letter spacing:

- Display: negative tracking from `-0.06em` to `-0.02em`.
- Metadata: `0`, because mono text already creates the machine tone.
- Body: `0`.

## 4. Grid And Layout

The core structure is a table. Use strict horizontal rules and vertical cuts.

Desktop web:

- outer border may wrap the whole canvas,
- page margin: `18-54px`,
- ruled rows: `44-220px`,
- content cells: 3, 4, 6, or 12 columns,
- avoid rounded containers.

Slides:

- 16:9 canvas,
- safe margin: `42-56px`,
- title rows can touch the canvas edge if the crop is intentional,
- readable text must stay inside cells,
- no more than four content cells per slide.

Composition patterns:

- Specimen Stack: two or three full-width display rows.
- Metadata Rail: tiny top row split into title, category, page number.
- Publisher Grid: bottom cells with author, date, index, format.
- Split Specimen: rust field on one side, pearl field on the other.
- Arrow Pair: large bracket-like arrows as a directional motif.

## 5. Shape Language

Allowed:

- horizontal and vertical rules,
- rectangles and square cells,
- large arrows,
- bracket marks,
- black bars,
- cropped words,
- simple typographic symbols.

Avoid:

- circles as decorative filler,
- gradients,
- blobs,
- rounded cards,
- drop shadows inside the design,
- ornamental illustrations.

Shapes should behave like typography or print marks. A mark must either label, divide, point, or frame.

## 6. UI Guidelines

This style can support a portfolio, campaign microsite, design studio page, landing page, or deck system. For real product UI, reduce the display type and keep only the grid, rules, square controls, and strong contrast.

Buttons:

- rectangular,
- square corners,
- black or rust fill,
- uppercase,
- 44-48px height,
- no pill shapes,
- use a visible border on secondary buttons.

Navigation:

- top metadata row,
- mono uppercase labels,
- short words only,
- avoid large nav menus,
- active state can be rust underline or filled cell.

Cards:

- should look like table cells,
- use borders instead of shadows,
- never nest cards inside cards,
- keep each cell to one idea.

Forms:

- square inputs,
- 2px black border,
- mono labels,
- rust focus outline,
- no floating labels.

## 7. Presentation Guidelines

Opening and section slides can be very bold. Business-content slides should keep the poster structure but reduce the font scale.

Good slide types:

- title specimen with huge word rows,
- market or portfolio index using grid cells,
- timeline as a ruled table,
- comparison matrix with black/rust headers,
- one-metric slide with oversized numerals.

Avoid:

- paragraph-heavy slides,
- five-color charts,
- tiny captions over rust,
- decorative icons,
- all-caps body copy longer than one line.

Minimum sizes for a 16:9 deck:

- metadata: 13px,
- body: 18px,
- cell heading: 24px,
- slide title: 54px,
- poster rows: 90px or larger.

## 8. Charts And Data

Charts should be table-like and direct.

Use:

- black axes,
- rust highlight,
- thick bars,
- direct labels,
- ruled backgrounds only when they help reading.

Avoid:

- default chart palettes,
- glossy effects,
- legends when labels fit directly,
- cramped annotation blocks.

## 9. Accessibility

- Keep pearl/ink as the default high-contrast pairing.
- Use rust for large text or filled panels, not tiny body copy on pearl.
- Do not rely on color alone for state; add border, underline, or label.
- Keep all interactive text at 14px minimum on web.
- On mobile, stack cells rather than shrinking display words into illegibility.

## 10. Reuse Checklist

Before shipping:

- Does the layout look like a ruled specimen sheet?
- Is the rust field intentional and limited?
- Are all paragraphs inside clean cells?
- Are huge words cropped deliberately?
- Are there no rounded cards, gradients, or decorative shadows?
- Can the mobile layout be read without horizontal scrolling?
- Does every mark divide, label, point, or frame something?
