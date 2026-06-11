# UFO Archive Paper Styleguide

## 1. Style Character

UFO Archive Paper turns the supplied black-background sighting posters into a UI and presentation system. It uses dark negative space, tall off-white paper panels, visible paper wrinkles, ultra-wide thin type, blunt archival headlines, and hand-measured elliptical trace lines.

It should feel:

- mysterious, but still readable,
- printed and physical, not glossy,
- archival rather than futuristic,
- quiet until the heavy report title appears,
- suited to portfolios, cultural pages, investigation decks, and editorial microsites.

Avoid using it for dense dashboards, cheerful launch pages, financial interfaces, or long-form product admin screens.

## 2. Core Rules

1. Start with a black void and place paper on top of it.
2. Use no rounded SaaS cards; panels should feel like thin printed sheets.
3. Pair one wirelike display face with one blunt heavy face.
4. Keep all body text monospaced or near-monospaced.
5. Use orbital line traces as the main graphic device.
6. Do not use the 12-column, split-pane, ruled-table, or chunky indexed layouts from the other packs.
7. Let paper texture be subtle. It should read as creases, not decoration.
8. Keep color nearly monochrome, with red or cyan only for small state or annotation moments.
9. Preserve large empty black fields around the paper.
10. Use short report-like copy instead of marketing language.

## 3. Palette

| Token | Hex | Role |
|---|---:|---|
| `--ua-black` | `#020202` | page and deck field |
| `--ua-void` | `#070707` | secondary black field |
| `--ua-paper` | `#F2F2EF` | primary printed surface |
| `--ua-paper-warm` | `#E6E4DF` | paper shadow and alternate surface |
| `--ua-paper-cool` | `#F8F8F6` | highlights and surface lift |
| `--ua-ink` | `#020202` | type and trace lines |
| `--ua-graphite` | `#242424` | dense body copy |
| `--ua-faint` | `#AAA9A4` | quiet metadata and texture |
| `--ua-red` | `#D63F2D` | rare alert or evidence mark |
| `--ua-cyan` | `#89AAA7` | rare observation annotation |

Recommended proportions:

- 45-60% black void,
- 30-45% paper,
- 5-15% ink line and typography,
- 0-5% red or cyan.

Do not add gradients as atmosphere, neon palettes, warm beige fields, or multi-color chart schemes.

## 4. Typography

Display wire face:

```css
font-family: "Michroma", "Eurostile", "Bank Gothic", "Trebuchet MS", sans-serif;
```

Heavy report face:

```css
font-family: "Bowlby One", "Arial Black", Impact, sans-serif;
```

Metadata and body:

```css
font-family: "Spline Sans Mono", "Courier New", monospace;
```

Hierarchy:

| Element | Size | Weight | Case | Notes |
|---|---:|---:|---|---|
| Paper cover word | 42-82px web, 54-64px slide | 400 | title case | wide, thin, line-broken |
| Report headline | 38-82px | 400 | mixed or title case | tight leading, blunt mass |
| Section heading | 28-46px | 400 | uppercase | heavy face only |
| Body report | 15-25px | 600 | sentence case | short paragraphs |
| Metadata | 11-13px | 700 | uppercase | small, direct, report-like |

Letter spacing should remain `0`. This style gets its spacing from the typeface width and the black field around it.

## 5. Layout

The primary layout is a poster pair, not a reusable column grid.

Desktop web:

- place one or two tall paper panels in a black field,
- use wide gaps between panels,
- keep the paper aspect ratio close to a tall handbill,
- use a simple strip or stack after the hero for supporting information,
- let mobile stack the paper panels vertically.

Slides:

- canvas: 16:9,
- preserve black margins around paper,
- use no more than two paper objects per slide,
- keep readable content inside the paper or in a single black-field note,
- let line traces occupy the empty half of a slide.

Composition patterns:

- Double Evidence: two tall paper sheets side by side.
- Case Packet: one paper block plus a large orbit trace.
- Report Strip: three compact notes under a large visual.
- Black Archive: title and metadata floating in black with a single sheet.

## 6. Motifs

Allowed:

- tall paper slabs,
- subtle crease lines,
- elliptical trace drawings,
- black ink strokes,
- tiny uppercase metadata,
- report dates and place names,
- small red or cyan evidence marks.

Avoid:

- icons,
- stock photos,
- decorative blobs,
- colorful cards,
- 12-column scaffolds,
- split Bauhaus circles,
- specimen-table cells,
- friendly rounded campaign shapes.

## 7. UI Guidance

This style is best for editorial or portfolio surfaces. For interactive UI, keep the system sparse.

Buttons:

- rectangular,
- black on paper or paper on black,
- uppercase mono label,
- 40-44px height,
- no pill shapes.

Panels:

- use paper surfaces, not cards,
- keep radius at 3px or less,
- do not nest panels,
- never put body copy over active trace lines.

Navigation:

- small uppercase mono text,
- top edge placement,
- short words only,
- active states can use underline, red dot, or paper inversion.

## 8. Presentation Guidance

Good slide types:

- two-panel poster cover,
- single report with orbital trace,
- incident timeline as compact paper notes,
- one oversized location/date headline,
- portfolio case study framed as an evidence packet.

Avoid:

- bullet-heavy slides,
- dense tables,
- multicolor data visualization,
- tiny captions over black,
- decorative trace lines behind paragraphs.

For a 16:9 deck:

- metadata: 12-13px,
- body: 17-22px,
- heavy title: 42-82px,
- wire title: 50-64px,
- line trace stroke: 3-4px.

## 9. Accessibility

- Keep body copy on paper for maximum contrast.
- Do not rely on texture to communicate state.
- Give line art `aria-hidden="true"` when it is decorative.
- Keep report copy short enough to avoid tiny type.
- On mobile, stack panels and preserve readable type sizes.

## 10. Reuse Checklist

Before shipping:

- Does the first read feel like black space plus paper evidence?
- Are the wire and heavy faces both present?
- Are the trace lines clear but not fighting the copy?
- Did you avoid borrowing another pack's grid or font system?
- Is all body text readable on mobile and slides?
- Could the page be printed as a stark archival poster?
