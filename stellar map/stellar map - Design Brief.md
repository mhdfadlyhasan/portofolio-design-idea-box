---
title: "stellar map - Design Brief"
status: draft
version: 0.1
updated: 2026-11-14
theme: stellar map
inherits: "_MASTER DESIGN BRIEF.md"
output: design-spec-only
tags:
  - design-brief
  - theme
  - stellar-map
---

# stellar map — Design Brief

The active direction. A portfolio read like a star chart: navigation by coordinates, proof plotted as constellations, contact as a fixed beacon.

Parent: [_Master Design Brief](../_MASTER%20DESIGN%20BRIEF.md) · Vocabulary: [Glossary](../Glossary.md) · Decisions: [Decision Log](../Decision%20Log.md) · Images: [`assets/references/`](../assets/references/)

---

## 1. Theme statement and positioning

- **One-line theme:** A portfolio read like a star chart — positions, clusters, and a beacon, not a menu of pages.
- **Metaphor:** Celestial cartography and celestial navigation.
- **Positioning:** Calm, precise, exploratory. Closer to a mission log or an almanac than a marketing site. Dark, quiet, data-literate.
- **What success looks like:** A first-time visitor locates who I am within one screen and feels oriented, as if reading a map that knows where they are.

## 2. Glossary researched by the user

Terms this design depends on. Full definitions in the [Glossary](../Glossary.md); the rationale here is what makes the term a design decision.

| Term | Why it matters here | Source |
| --- | --- | --- |
| Cartography | The site is a map, so the priority is a readable legend and consistent plotting, not decoration. | [Glossary](../Glossary.md) |
| Star chart | Projects become plotted points and constellation lines, giving work a spatial memory. | [Glossary](../Glossary.md) |
| Constellation | Groups related work into named clusters, so the eye reads themes rather than a flat grid. | [Glossary](../Glossary.md) |
| Celestial sphere | A full-bleed, curved field lets content sit in space instead of in boxes. | [Glossary](../Glossary.md) |
| Equatorial coordinate system | Anchors and labels can use a consistent two-axis notation, making navigation feel measured. | [Glossary](../Glossary.md) |
| Parallax | Depth on scroll supports the spatial metaphor — but only if reduced-motion is respected. | [Glossary](../Glossary.md) |
| Ephemeris | The experience section reads as dated almanac rows, reinforcing precision. | [Glossary](../Glossary.md) |
| Astrolabe | Instrument chrome (rings, scales, crosshairs) gives the hero a tool-like identity. | [Glossary](../Glossary.md) |
| HUD | Small overlay labels add atmosphere; they must never reduce legibility. | [Glossary](../Glossary.md) |
| Beacon | The single persistent contact signal; one action, always findable. | [Glossary](../Glossary.md) |
| Wayfinding | Navigation's job is orientation and next step, not a list of links. | [Glossary](../Glossary.md) |

_User research note: expand this table with at least one primary source per term and a sentence on what was learned. Seed rows taken from the shared glossary._

## 3. Color palette

Dark, low-glare, high-contrast. Color is used for signal, not surface decoration.

### Tokens
| Token | Hex | RGB | Role | Contrast on bg |
| --- | --- | --- | --- | --- |
| color-bg | `#05070D` | 5, 7, 13 | page background (void) | — |
| color-surface | `#0B1220` | 11, 18, 32 | cards, panels | 1.4:1 (surface only) |
| color-text | `#E8EEF7` | 232, 238, 247 | primary text | 16.1:1 |
| color-text-muted | `#8A97AB` | 138, 151, 171 | meta, captions | 6.4:1 |
| color-accent | `#5CE1E6` | 92, 225, 230 | ion cyan — primary action | 12.2:1 |
| color-accent-2 | `#F2B455` | 242, 180, 85 | comet amber — secondary highlight | 10.1:1 |
| color-border | `#1C2938` | 28, 41, 56 | dividers, grid lines | 1.7:1 (non-text) |
| color-focus | `#9AE6FF` | 154, 230, 255 | focus ring | 13.4:1 |
| color-success | `#6EE7A8` | 110, 231, 168 | status | 12.6:1 |
| color-warning | `#F2B455` | 242, 180, 85 | status (shares amber) | 10.1:1 |
| color-error | `#FF7A7A` | 255, 122, 122 | status | 7.3:1 |

Contrast values are approximate (WCAG relative luminance) and must be re-verified before build.

### Combination examples

| Combination | Swatches | Where used | Do | Don't |
| --- | --- | --- | --- | --- |
| Void + starlight | `bg` / `text` | all body copy | long-form reading | tint body text |
| Void + ion cyan | `bg` / `accent` | primary CTA, active nav | one focal action per view | outline every element |
| Ion cyan fill + void text | `accent` / `bg` | filled buttons | short labels only | long sentences |
| Surface + comet amber | `surface` / `accent-2` | tags, timestamps | small labels | large background fills |
| Void + muted slate | `bg` / `text-muted` | captions, coordinates | supporting info | primary content |
| Void + border | `bg` / `border` | grid lines, dividers | faint, low emphasis | strong contrast lines |

Render these as swatch strips and store in [`assets/references/`](../assets/references/).

## 4. Typography and iconography

- **Display face:** Space Grotesk — geometric, technical, slightly idiosyncratic; suits coordinate labels. Fallback: `system-ui, sans-serif`.
- **Body face:** Inter — high legibility at small sizes on dark backgrounds. Fallback: `system-ui, sans-serif`.
- **Mono / data face:** IBM Plex Mono — reads as instrument readout; used for coordinates, tags, timestamps. Fallback: `ui-monospace, monospace`.
- **Scale overrides:** none; inherit [master scale](../_MASTER%20DESIGN%20BRIEF.md).
- **Iconography:** 1.5px stroke line icons, rounded joins; celestial motifs (rings, dots, crosshairs) drawn as simple strokes. Consistent 24px grid; no filled or multicolor icons.

## 5. Design ideas sourced from the glossary

| # | Design idea | Glossary term(s) | Why it works | Reference image |
| --- | --- | --- | --- | --- |
| 1 | Projects plotted as points, related work joined by faint constellation lines | Star chart, Constellation | Turns a list into a readable map; grouping becomes spatial. | _to add_ |
| 2 | Faint RA/Dec grid behind the hero, denser at edges | Celestial sphere, Equatorial coordinates | Signals "map" before reading a word; low contrast keeps text dominant. | _to add_ |
| 3 | Section anchors labeled as coordinates (`RA 04h 12m`) | Equatorial coordinates, Cartography | Makes navigation feel measured and consistent; memorable anchors. | _to add_ |
| 4 | Experience rendered as ephemeris rows with dates and short entries | Ephemeris, Nautical almanac | Precision and calm; avoids the generic timeline. | _to add_ |
| 5 | Layered starfield with slow parallax on scroll | Parallax | Adds depth without clutter; must reduce to static under reduced motion. | _to add_ |
| 6 | Minimal astrolabe ring framing the hero name | Astrolabe | Gives the hero an instrument identity; anchors the page. | _to add_ |
| 7 | HUD-style micro-labels (status, coordinates, version) | HUD, Telemetry | Atmosphere and orientation; decorative only, never required info. | _to add_ |
| 8 | Radar-sweep reveal on work hover | HUD, Telemetry | Makes interaction feel like scanning; respect reduced motion. | _to add_ |
| 9 | Persistent beacon button for contact | Beacon, Wayfinding | One always-findable action; reduces hunting. | _to add_ |
| 10 | Nav as a compass strip (N/E/S/W mapped to sections) | Wayfinding, Horizontal coordinates | Reinforces orientation; use only if labels stay obvious. | _to add_ |

## 6. Imagery and art direction

- **Mood:** quiet, vast, precise, instrumented, cold-but-warm-accented.
- **Subject matter:** real astrophotography, star fields, orbital diagrams, instrument detail. Avoid fantasy space art and lens-flare clichés.
- **Treatment:** deep blacks, slight grain, desaturate unless the image is a focal accent; overlay a subtle vignette.
- **Sourcing rule:** public-domain and permissively licensed imagery only (NASA, ESA/ESO with attribution). Reference-only copyrighted art is never shipped.
- **Moodboard:** embed selected images from [`assets/references/`](../assets/references/).

## 7. Layout and component inventory

| Component | Reuses global? | Theme override |
| --- | --- | --- |
| Header / nav | yes | compass strip; mono labels |
| Card (work) | yes | plotted-point / constellation treatment |
| Button | yes | filled ion-cyan primary; ghost with hairline border |
| Tag | yes | mono, amber on surface |
| Timeline | no | replaced by ephemeris rows |
| Section wrapper | yes | coordinate label above title |

## 8. Page and section spec

Follow the [master output contract](../_MASTER%20DESIGN%20BRIEF.md#0-how-to-use-this-document). Scaffolds below; fill content later.

### Hero
- **Purpose:** state name, role, and positioning in one screen.
- **Content blocks:** name (must), role (must), one-line positioning (must), primary CTA "View work" (must), beacon/contact (should).
- **Visual hierarchy:** 1st name, 2nd positioning line, 3rd CTA.
- **Layout:** full viewport; centered column; astrolabe ring behind name; RA/Dec grid at low opacity.
- **Tokens:** `type-display`, `color-text`, `color-accent`, `color-border`.
- **States:** default; CTA hover (accent fill), focus ring.
- **Motion:** slow ring rotation (60s, linear), starfield parallax; both disabled under reduced motion.
- **Accessibility:** text over imagery must keep 4.5:1; ring is decorative and `aria-hidden`.
- **Open questions:** is a portrait used, or typography only?

### Selected work
- **Purpose:** prove capability through three to five projects.
- **Content blocks:** section title, constellation cluster(s), project points with title/role/year, inline or linked detail.
- **Visual hierarchy:** 1st cluster shape, 2nd project titles, 3rd meta.
- **Layout:** desktop 3-up clusters; tablet 2-up; mobile single column list with constellation line removed.
- **Tokens:** `color-accent`, `color-accent-2`, `type-mono`.
- **States:** default, hover (radar sweep + label), focus, empty.
- **Motion:** line draw on enter; hover sweep ≤ 240ms.
- **Accessibility:** each point is a real link with visible focus; hover effect is not the only cue.
- **Open questions:** sub-page vs inline expand (see [Decision Log](../Decision%20Log.md)).

### About
- **Purpose:** context and point of view.
- **Content blocks:** short bio, approach sentence, optional portrait.
- **Visual hierarchy:** 1st lede, 2nd body, 3rd portrait.
- **Layout:** two columns desktop, stacked mobile.
- **Tokens:** `type-body`, `color-text-muted`.
- **States:** static.
- **Motion:** fade-up on enter.
- **Accessibility:** portrait alt text.
- **Open questions:** length limit.

### Capabilities
- **Purpose:** show what I can do, grouped.
- **Content blocks:** named clusters of skills.
- **Visual hierarchy:** cluster names, then items.
- **Layout:** tag clusters; 3 columns desktop, stack mobile.
- **Tokens:** `color-surface`, `color-accent-2`, `type-mono`.
- **States:** tag hover, focus.
- **Motion:** none beyond hover.
- **Accessibility:** tags are text, not icons alone.
- **Open questions:** which clusters.

### Process
- **Purpose:** show how I work.
- **Content blocks:** three to five steps.
- **Visual hierarchy:** step numbers, then labels.
- **Layout:** horizontal orbit line desktop, vertical mobile.
- **Tokens:** `color-border`, `color-accent`.
- **States:** default, hover.
- **Motion:** progress line on scroll.
- **Accessibility:** reading order matches visual order.
- **Open questions:** number of steps.

### Experience
- **Purpose:** credibility.
- **Content blocks:** ephemeris rows: date, role, org, one line.
- **Visual hierarchy:** dates, roles, then org.
- **Layout:** table on desktop; stacked rows on mobile.
- **Tokens:** `type-mono`, `color-text-muted`, `color-border`.
- **States:** row hover, focus if linked.
- **Motion:** none required.
- **Accessibility:** real table semantics on desktop; label/value pairs on mobile.
- **Open questions:** include education?

### Contact
- **Purpose:** convert interest into a message.
- **Content blocks:** invitation line, email, socials, beacon CTA.
- **Visual hierarchy:** invitation, email, socials.
- **Layout:** centered, generous space.
- **Tokens:** `color-accent`, `color-focus`.
- **States:** default, hover, focus, copied-email confirmation.
- **Motion:** none.
- **Accessibility:** email as real `mailto:` link; copy button announced.
- **Open questions:** form vs email only.

## 9. Motion

| Element | Trigger | Duration | Easing | Reduced-motion fallback |
| --- | --- | --- | --- | --- |
| Starfield parallax | scroll | continuous | linear | static layers |
| Astrolabe ring | load / idle | 60s loop | linear | static |
| Constellation line draw | enter viewport | 480ms | ease-out | instant appear |
| Radar sweep on work | hover | 240ms | ease-out | static label change |
| Section fade-up | enter viewport | 240ms | ease-out | instant |
| Beacon pulse | idle | 3s loop | ease-in-out | no pulse |

## 10. Assets and references

| Asset | File | Source | License | Used in |
| --- | --- | --- | --- | --- |
| Star field backdrop | _to add_ | [NASA Image Library](https://images.nasa.gov/) | public domain | hero, background |
| Deep-field texture | _to add_ | [ESA/ESO](https://www.eso.org/public/images/) | CC BY (attribution) | sections |
| Astrolabe reference | _to add_ | _to add_ | _verify_ | hero chrome |
| Star chart reference | _to add_ | _to add_ | _verify_ | work clusters |
| Arknights Endfield cues | [reference note](../Arknights%20endfield/Reference%20-%20Arknights%20Endfield.md) | _to add_ | reference only, do not ship | HUD/labels |

## 11. Open questions and decisions

- Open questions tracked in the [Decision Log](../Decision%20Log.md).
- Decisions tracked in the [Decision Log](../Decision%20Log.md).

## 12. Acceptance checklist

- [x] Glossary rows each have a source and rationale.
- [x] Palette includes roles, contrast values, and combination examples.
- [x] Design ideas cite glossary terms (images pending).
- [x] Typography, iconography, and imagery direction defined.
- [x] Every section follows the output contract scaffold.
- [x] All states and breakpoints specified.
- [x] Accessibility notes present.
- [x] No code in the spec.
