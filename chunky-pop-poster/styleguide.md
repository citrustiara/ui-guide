# Chunky Pop Poster Styleguide

## 1. Style Character

Chunky Pop Poster is a loud, rounded, campaign-first style inspired by retro type specimen posters, saturated palette variants, friendly launch graphics, and bright product-drop art. It is deliberately warmer and more playful than the Swiss Grid, less geometric than the Futura/Bauhaus kit, and less strict than the Modern Display Specimen system.

The style should feel:

- big and immediate,
- friendly rather than corporate,
- promotional without becoming messy,
- editorial enough to hold a portfolio,
- simple underneath the visual loudness.

Use it for launch pages, creator portfolios, small brand systems, campaign microsites, social-first decks, and product-drop pages. Avoid it for dense dashboards, legal/compliance interfaces, finance products, and serious internal enterprise tools.

## 2. Core Rules

1. Start with one enormous rounded word or phrase.
2. Use a bright field color as the main atmosphere.
3. Add only one secondary motif per section: dot, loop, color chip, or round label.
4. Keep body copy short and high contrast.
5. Use simple rows and index blocks under the expressive hero.
6. Let type be soft and heavy, but keep layout alignment exact.
7. Do not stack multiple decorative motifs in one area.
8. Keep corners either circular or lightly rounded; avoid soft SaaS cards.
9. Use handwritten loops only as a single accent, never as paragraph decoration.
10. If a layout starts feeling chaotic, remove shapes before shrinking the text.

## 3. Palette

| Token | Hex | Role |
|---|---:|---|
| `--cp-sky` | `#2787D8` | primary poster field |
| `--cp-sky-deep` | `#0F5FAE` | darker blue accents and numbers |
| `--cp-butter` | `#ECF558` | oversized display type and highlights |
| `--cp-guava` | `#FF5A3F` | warm callouts and contrast panels |
| `--cp-pink` | `#F6B4D2` | green/pink palette pairing and soft accents |
| `--cp-mint` | `#087C42` | secondary green field |
| `--cp-cream` | `#FFF8EF` | main readable surface |
| `--cp-ink` | `#11131B` | text, borders, and strong buttons |
| `--cp-muted` | `#5B6172` | body copy |

Recommended proportions:

- 35-50% sky or cream,
- 20-35% butter or guava display color,
- 10-20% ink,
- 5-10% pink, mint, or small accent shapes.

Avoid adding gradients, purple, beige monotone fields, or more than one extra accent color.

## 4. Typography

Recommended CSS stack:

```css
font-family: "Fredoka", "Arial Rounded MT Bold", "Trebuchet MS", Arial, sans-serif;
```

Use a rounded or bulbous display face for headlines. Fredoka is used in the examples because it feels softer and less industrial than the other style kits. Body text should stay simple and readable.

Hierarchy:

| Element | Desktop Size | Weight | Case | Notes |
|---|---:|---:|---|---|
| Poster word | 96-150px | 900 | uppercase | 1-3 short lines |
| Slide title | 56-72px | 900 | uppercase | short, expressive |
| Section title | 42-78px | 900 | uppercase | use sparingly |
| Tile heading | 24-30px | 900 | uppercase | compact blocks |
| Body | 16-18px | 700 | sentence case | short paragraphs only |
| Metadata | 12-13px | 800-900 | uppercase | monospaced or compact |

Letter spacing should stay at `0` for display and body text. Use weight, scale, and color instead of tight tracking.

## 5. Layout

The style uses simple poster composition rather than strict Swiss density.

Desktop web:

- max page width: `1440px`,
- hero padding: `56-72px`,
- readable body columns under `560px`,
- use 2-column or 4-column sections after the hero,
- keep one strong vertical or horizontal break per section.

Slides:

- canvas: `16:9`,
- safe margin: `48-64px`,
- hero word can take 60-70% of the slide,
- body copy should stay in one short block,
- secondary shapes should sit near, not on top of, the main title.

## 6. Motifs

Allowed:

- large dot,
- round label,
- rounded badge,
- one casual loop line,
- thick display word,
- cream information band,
- numbered index row.

Avoid:

- many small icons,
- gradients,
- photo collages,
- bokeh or orb backgrounds,
- long handwritten scripts,
- dense tables,
- heavily shadowed cards.

## 7. UI Guidance

This style can work in interfaces, but only when the UI is simple. It is best for marketing and portfolio surfaces.

Buttons:

- rectangular or lightly rounded,
- ink fill with butter hover,
- uppercase labels,
- 44-52px height,
- avoid tiny icon-only actions.

Panels:

- use sharp borders or 8px radius,
- no nested card stacks,
- use large color fields for priority,
- avoid subtle grey-on-grey SaaS styling.

Navigation:

- short uppercase labels,
- no pill nav,
- numeric sections such as `01`, `02`, `03`,
- keep active state loud but singular.

Forms:

- cream fields on colored backgrounds,
- ink borders,
- large labels,
- use guava for errors and butter for positive highlights.

## 8. Presentation Guidance

Good slide types:

- poster cover with one huge phrase,
- case study slide with a color rail and two metrics,
- campaign index with numbered tiles,
- launch offer with one round label or color chip,
- before/after slide using two big color fields.

Avoid:

- more than 4 bullets on a slide,
- body text over the poster word,
- decorative motifs on every slide,
- tiny legends,
- charts with many series.

For data slides, make one number the focus and use direct labels. If a chart needs more than three colors, this is probably the wrong style.

## 9. Accessibility

- Keep all body text on cream or deep ink fields.
- Do not put small cream text on butter.
- Treat butter as a display color, not a body background.
- Keep round-label text large enough to read.
- Do not rotate important labels more than a few degrees.
- Use responsive breakpoints instead of allowing display words to escape the viewport.

## 10. Example Files

- `tokens.css` - shared palette, typography, and reusable tokens.
- `home.html` - short portfolio/launch home page example.
- `example-deck.html` - two-slide presentation example with keyboard navigation.
