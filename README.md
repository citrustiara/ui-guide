# UI Guide

A curated library of editable visual style packs for people and AI agents building landing pages, portfolios, dashboards, and slide decks. Each pack includes design rules, CSS tokens, and small HTML examples that can be copied, adapted, or used as inspiration.

This repo is both:

- **A template/inspiration library for humans**: browse a pack, open the examples, copy the tokens, and adapt the layout.
- **A lightweight Agent Skill**: agents can load [`SKILL.md`](SKILL.md) to choose the right pack and follow the style constraints.

## Visual showcase

Browse the screenshot gallery in [`SHOWCASE.md`](SHOWCASE.md), including homepage and deck previews for every curated pack.

| Curated example | Traditional vibecoded baseline |
|---|---|
| <img src="swiss-grid/preview/home.png" alt="Swiss Grid homepage screenshot" width="340"> | <img src="vibecoded-glassmorphism/preview/home.png" alt="Vibecoded glassmorphism homepage screenshot" width="340"> |

The [`vibecoded-glassmorphism`](vibecoded-glassmorphism/) folder is included only as a comparison baseline. It intentionally uses a generic modern glassmorphism look and does not import any curated pack tokens or styles.

## Style packs

| Pack | Character | Best for | Start here |
|---|---|---|---|
| [`swiss-grid`](swiss-grid/) | Technical, analytical, restrained, grid-led, black/white with red accent | Business reports, serious product decks, dashboards, B2B pages | [`styleguide.md`](swiss-grid/styleguide.md), [`home.html`](swiss-grid/home.html), [`example-deck.html`](swiss-grid/example-deck.html) |
| [`futura-bauhaus`](futura-bauhaus/) | Bold geometric Bauhaus composition with strong type, circles, bars, and primary-color energy | Editorial product storytelling, portfolios, brand concepts, confident decks | [`styleguide.md`](futura-bauhaus/styleguide.md), [`home.html`](futura-bauhaus/home.html), [`example-deck.html`](futura-bauhaus/example-deck.html) |
| [`modern-display-specimen`](modern-display-specimen/) | Hard-edged display typography, oxidized rust, pearl, black ink, muted silver | Creative portfolios, fashion/culture pages, type-led launch pages, striking title slides | [`styleguide.md`](modern-display-specimen/styleguide.md), [`home.html`](modern-display-specimen/home.html), [`example-deck.html`](modern-display-specimen/example-deck.html) |
| [`chunky-pop-poster`](chunky-pop-poster/) | Bright, friendly, rounded, retro poster-inspired, promotional | Product drops, creator pages, playful launches, expressive presentation openings | [`styleguide.md`](chunky-pop-poster/styleguide.md), [`home.html`](chunky-pop-poster/home.html), [`example-deck.html`](chunky-pop-poster/example-deck.html) |
| [`ufo-archive-paper`](ufo-archive-paper/) | Dark archival poster system with paper panels, investigative tone, atmospheric contrast | Mysterious narratives, archival storytelling, research dossiers, cinematic decks | [`styleguide.md`](ufo-archive-paper/styleguide.md), [`home.html`](ufo-archive-paper/home.html), [`example-deck.html`](ufo-archive-paper/example-deck.html) |

## Folder contract

Each style pack follows the same structure:

```txt
style-pack/
  README.md          # short overview and preview instructions
  styleguide.md      # detailed design rules and usage guidance
  tokens.css         # reusable CSS variables, primitives, and utilities
  home.html          # editable web/landing-page example
  example-deck.html  # editable two-slide HTML deck example
  preview/           # rendered screenshots for gallery/docs
```

The comparison baseline follows the same homepage/deck preview convention but is not a selectable style pack.

## Preview locally

Open any example directly in a browser:

```txt
swiss-grid/home.html
swiss-grid/example-deck.html
```

For slide decks:

- Use left/right arrow keys to move between slides.
- Add `?qa=1` to hide navigation for screenshots.
- Some decks also support `?qa=1&slide=2` to open a specific slide directly.

If a browser blocks local assets, serve the repo locally:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000/<pack-name>/home.html`.

## How people should use this repo

1. Pick a style pack that matches the tone of the project.
2. Read the pack's `README.md` and `styleguide.md`.
3. Open `home.html` or `example-deck.html` to inspect the layout patterns.
4. Copy or import `tokens.css` into your project.
5. Replace placeholder content while preserving the pack's typography, color, spacing, and composition rules.
6. Avoid mixing packs unless you are intentionally creating a hybrid direction.

## How AI agents should use this repo

Agents should load [`SKILL.md`](SKILL.md), then:

1. Identify the requested output type: landing page, deck, dashboard, portfolio, visual direction, etc.
2. Choose the closest style pack, or present 2-3 options if the request is ambiguous.
3. Read the chosen pack's `README.md`, `styleguide.md`, `tokens.css`, and the relevant HTML example.
4. Reuse the pack's tokens and layout patterns instead of inventing a new style from scratch.
5. Keep styles internally consistent. Do not combine packs unless the user asks.
6. Deliver editable output with clear paths and note which pack was used.

## Use as a Pi skill

This repo includes a root [`SKILL.md`](SKILL.md), so it can be loaded as a single Agent Skill.

From Pi, load it explicitly:

```bash
pi --skill /path/to/UIguide
```

Or copy/symlink this repo into a skill discovery folder such as:

```txt
~/.pi/agent/skills/ui-guide/
~/.agents/skills/ui-guide/
```

The skill is intentionally lightweight: it indexes the packs and describes the workflow, while the detailed design knowledge remains inside each style pack.

## Adding a new style pack

When adding a pack, keep the same contract:

- `README.md` with character, files, and preview notes.
- `styleguide.md` with detailed rules for color, type, layout, components, imagery, and usage.
- `tokens.css` with named variables and reusable primitives.
- `home.html` as an editable page example.
- `example-deck.html` as an editable deck example.

Then update:

- This root `README.md` style-pack table.
- [`SKILL.md`](SKILL.md) pack-selection table.

## Notes

- These are editable templates and visual systems, not production-ready component libraries.
- Check licensing for any external fonts, images, or assets before public/commercial use.
- Add a repository `LICENSE` file before distributing this repo publicly.
