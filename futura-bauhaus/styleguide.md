# Futura Bauhaus Styleguide

## 1. Style Character

This style is a bold, geometric, Bauhaus-inspired system for portfolio pages, visual identities, editorial landing pages, and high-impact presentation openings. It is inspired by the Futura type showcase poster: split color fields, cropped letterforms, perfect circles, thick arcs, sharp contrast, and text arranged as engineered blocks.

The style should feel:

- constructed, not decorated,
- geometric, but still readable,
- poster-like on opening moments,
- disciplined and modular once content gets dense,
- loud in composition, restrained in palette.

Use it when the brand can carry confidence and visual force. Avoid it for dashboards, compliance-heavy tools, long legal documents, or interfaces where users need calm repetition for hours.

## 2. Core Rules

1. Build the page from rectangles, circles, half-circles, and large cropped type.
2. Use only one loud accent: coral red.
3. Keep corners sharp. Rounded cards weaken the language.
4. Use uppercase metadata, but keep body text sentence case.
5. Let one oversized shape dominate the first viewport or title slide.
6. Keep text short. If the paragraph becomes long, move to a quieter grid section.
7. Use asymmetry, but align everything to a clear modular grid.
8. Never place paragraph text over complex geometry.
9. Prefer split-screen tension over gradients.
10. Use negative space as a real design object.

## 3. Palette

| Token | Hex | Role |
|---|---:|---|
| `--fb-white` | `#FFFFFF` | main poster field |
| `--fb-paper` | `#F8F7F2` | page background outside cards/canvases |
| `--fb-red` | `#FF4D4A` | Bauhaus coral accent and red panels |
| `--fb-red-dark` | `#D92F2C` | hover, pressed, or darker red labels |
| `--fb-navy` | `#030936` | main dark field, typography, arcs |
| `--fb-navy-soft` | `#161B4D` | secondary navy surface |
| `--fb-muted` | `#5F6475` | body copy and annotations |
| `--fb-line` | `#D9DBE3` | fine construction lines |

Recommended proportions:

- 40-55% white or paper,
- 25-40% navy or red field,
- 10-20% large geometric forms,
- 5-10% body text and metadata.

Do not add extra blues, purples, beige gradients, or decorative shadows. If you need a third signal color, use it only inside charts, not as visual branding.

## 4. Typography

Recommended CSS stack:

```css
font-family: "Jost", "Avenir Next", "Futura", "Trebuchet MS", Arial, sans-serif;
```

Jost is used because it is freely available and has the geometric feel needed for this system. Futura is suitable when licensed locally.

Hierarchy:

| Element | Size | Weight | Case | Notes |
|---|---:|---:|---|---|
| Poster word | 90-180px | 900 | uppercase | crop at edges intentionally |
| Slide title | 56-104px | 900 | uppercase | short, one idea |
| Section title | 32-56px | 900 | uppercase | compact and loud |
| Accent sentence | 22-34px | 600 | sentence case | usually coral red |
| Body | 14-18px | 400-500 | sentence case | never all caps |
| Metadata | 10-12px | 800 | uppercase | date, index, labels |

Letter spacing:

- Display words: `0.08em` to `0.16em`.
- Metadata: `0.08em` to `0.14em`.
- Body: `0`.

## 5. Grid And Composition

Use a 12-column grid for desktop and slide layouts. The system works best when one or two elements break the grid by cropping, while all readable content stays aligned.

Desktop web:

- outer margin: `48-72px`,
- gutters: `20-32px`,
- sections: split `50/50`, `7/5`, or `8/4`,
- keep body columns under `620px`.

Slides:

- canvas: `16:9`,
- safe margin: `56-80px`,
- title block: max 55-65% width unless it is intentionally cropped,
- dense content: two or three blocks max,
- footer metadata optional and tiny.

Composition patterns:

- Split Field: white left, red or navy right.
- Center Ring: a circle cut by the split line.
- Cropped Word: letters extend beyond canvas edge.
- Index Blocks: large pale numbers behind content.
- Rule Bar: short horizontal rules used as anchors.

## 6. Geometry

Use geometric forms as structure, not decoration.

Allowed:

- full circle,
- split circle,
- half-circle,
- oversized arc,
- square blocks,
- thick horizontal or vertical bars,
- small dot as an index marker.

Avoid:

- gradients,
- freeform blobs,
- soft bokeh,
- ornamental line art,
- casual hand-drawn marks,
- rounded pill chips.

Shape rules:

- Circle stroke should be thick: `32-84px` depending on canvas.
- Arcs may crop off the edge by 20-60%.
- If a shape crosses two color fields, reverse color on each side.
- Do not let shapes touch important paragraph text.

## 7. UI Guidelines

This style can work for a homepage, brand microsite, portfolio, pitch intro, or campaign landing page. For actual product UI, reduce the poster behavior and keep only:

- sharp panels,
- geometric navigation,
- uppercase labels,
- red active state,
- navy primary actions,
- strong grid alignment.

Buttons:

- rectangular,
- no radius,
- uppercase label,
- 44-52px height,
- navy or red fill,
- avoid icon-only controls unless the icon is extremely familiar.

Cards and panels:

- use square bordered panels,
- avoid nested cards,
- avoid shadows except for very light page separation,
- do not use pale rounded SaaS cards.

Forms:

- square inputs,
- 2px border,
- clear labels above fields,
- red for focus only when active,
- navy submit button.

Navigation:

- compact uppercase metadata style,
- numeric index labels such as `01`, `02`, `03`,
- use rules or bars instead of soft dividers.

## 8. Presentation Guidelines

Opening slides may be loud. Content slides should be more controlled.

Good slide types:

- title with split field and cropped word,
- manifesto slide with one red accent sentence,
- portfolio/project index with giant numbers,
- case study slide with one large metric and two supporting blocks,
- comparison slide with thick bars and square panels.

Avoid:

- many bullet points,
- small text over red,
- decorative shapes behind dense tables,
- too many colors in charts,
- large paragraphs that fight the poster scale.

For a 16:9 deck:

- minimum text size: 18px,
- body text: 22-28px,
- section headings: 40-56px,
- display headings: 72-110px,
- keep a `56px` safe area around all readable content.

## 9. Charts And Data

Charts should look engineered and poster-like without losing meaning.

Use:

- navy axes,
- coral red highlight,
- thick bars,
- direct labels,
- no legends if labels fit near marks,
- grid lines only when they help comparison.

Avoid:

- Excel defaults,
- multi-color palettes,
- 3D effects,
- tiny axis labels,
- labels placed inside cramped bars.

## 10. Accessibility

- Do not set paragraph text below 14px on web or 18px on slides.
- Do not place red body text on navy unless the size is large and contrast is checked.
- Keep all interactive controls keyboard reachable.
- When using cropped display type, repeat the actual title in accessible readable text.
- For motion, use simple transforms only and respect reduced-motion settings.

## 11. Reuse Checklist

Before shipping:

- Is there one clear visual focus?
- Are all readable text blocks inside safe margins?
- Are shapes cropped intentionally, not accidentally?
- Is the palette limited to white, navy, coral, and neutral grey?
- Are body paragraphs readable without zoom?
- Does the mobile layout stack without hiding content?
- Would removing one shape make the page clearer? If yes, remove it.
