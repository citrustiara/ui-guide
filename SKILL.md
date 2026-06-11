---
name: ui-guide
description: Reusable UI and presentation style-guide/template library. Use when designing or adapting web pages, landing pages, dashboards, slide decks, visual directions, or component concepts from curated style packs such as Swiss Grid, Futura Bauhaus, Modern Display Specimen, Chunky Pop Poster, and UFO Archive Paper.
---

# UI Guide Skill

Use this skill when the user asks for a visual direction, style guide, UI mockup, landing page, portfolio page, dashboard concept, slide deck, or design-system-inspired implementation.

This repository is a library of style packs. Each pack contains:

- `README.md` - quick overview and preview notes.
- `styleguide.md` - detailed visual rules and design guidance.
- `tokens.css` - reusable CSS variables, primitives, and utility classes.
- `home.html` - editable web/landing-page example.
- `example-deck.html` - editable HTML deck example.

## Core rules

1. Use one style pack at a time unless the user explicitly asks for a hybrid.
2. Treat the chosen pack's `styleguide.md` as the source of truth.
3. Reuse the pack's `tokens.css` values and layout patterns instead of inventing unrelated colors, fonts, spacing, or components.
4. Preserve the pack's constraints. The constraints are part of the style.
5. If the request is ambiguous, offer 2-3 suitable packs with a short reason for each, then proceed with the best fit if the user has not specified.
6. Keep outputs editable and practical: clear HTML/CSS, copyable tokens, and minimal hidden dependencies.

## Pack selection guide

| Pack | Use when the work should feel like... | Strong for | Avoid for |
|---|---|---|---|
| `swiss-grid` | Technical, analytical, calm, precise, editorially restrained | B2B decks, reports, dashboards, product strategy, serious landing pages | Playful consumer launches, maximalist visuals |
| `futura-bauhaus` | Bold, geometric, graphic, modernist, poster-like | Brand concepts, portfolio pages, product narratives, confident presentation openers | Dense enterprise dashboards, subdued compliance content |
| `modern-display-specimen` | Type-led, sharp, cultural, fashion/editorial, high-contrast | Creative portfolios, striking landing pages, art/culture projects, title-heavy decks | Conventional SaaS UI, long-form documentation |
| `chunky-pop-poster` | Friendly, bright, rounded, retro, promotional, energetic | Product drops, creator launches, campaign pages, expressive deck sections | Finance/admin tools, dense analytical interfaces |
| `ufo-archive-paper` | Archival, mysterious, investigative, cinematic, dark-paper dossier | Research narratives, dossiers, atmospheric presentations, speculative storytelling | Cheerful brands, medical/compliance dashboards, light corporate pages |

## Comparison baseline

`vibecoded-glassmorphism/` is included only for visual comparison against a traditional generic AI-coded glassmorphism interface. Do not select it as a style pack unless the user explicitly asks for that baseline or asks for generic glassmorphism. It does not import or reuse the curated pack tokens.

## Workflow

1. **Understand the request**
   - Identify output type: page, deck, dashboard, component, brand direction, etc.
   - Identify desired tone: serious, playful, editorial, mysterious, geometric, analytical, etc.
   - Note constraints: framework, dimensions, content length, audience, accessibility, and delivery format.

2. **Choose a pack**
   - If the user names a pack, use it.
   - If the user describes a tone, pick the closest pack from the selection guide.
   - If multiple packs fit, briefly compare them and choose one unless the user wants options.

3. **Read the pack files before creating output**
   - Always read `<pack>/README.md`.
   - Always read `<pack>/styleguide.md` for rules and constraints.
   - Read `<pack>/tokens.css` before writing CSS.
   - Read `<pack>/home.html` for page work.
   - Read `<pack>/example-deck.html` for deck work.

4. **Adapt, do not dilute**
   - Keep the pack's palette, typography, spacing, borders, shapes, and composition logic.
   - Replace placeholder content with the user's content.
   - Add only components that fit the pack's rules.
   - Do not add generic gradients, shadows, rounded cards, stock SaaS patterns, emoji decoration, or mismatched fonts unless the selected pack explicitly supports them.

5. **Quality pass**
   - Verify the result still resembles the selected pack.
   - Check readable contrast and responsive behavior when relevant.
   - Confirm deck navigation or page links still work if modifying HTML examples.
   - State which pack was used and which files were changed or created.

## Common usage patterns

### Create a landing page

1. Choose the best pack.
2. Read the pack's `README.md`, `styleguide.md`, `tokens.css`, and `home.html`.
3. Copy/adapt `home.html` and `tokens.css` into the target location.
4. Replace content and adjust sections while preserving the pack's visual grammar.

### Create a slide deck

1. Choose the best pack.
2. Read the pack's `README.md`, `styleguide.md`, `tokens.css`, and `example-deck.html`.
3. Copy/adapt `example-deck.html`.
4. Preserve slide dimensions, navigation, and visual rhythm unless the user requests otherwise.

### Create a new style pack

Use the existing folders as references and create:

```txt
new-style-pack/
  README.md
  styleguide.md
  tokens.css
  home.html
  example-deck.html
```

Then update the root `README.md` and this `SKILL.md` with the new pack.
