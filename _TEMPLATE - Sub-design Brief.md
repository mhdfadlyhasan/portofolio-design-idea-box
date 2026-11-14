---
title: "Sub-design Brief Template"
status: template
version: 0.1
updated: 2026-11-14
theme: ""
inherits: "_MASTER DESIGN BRIEF.md"
output: design-spec-only
tags:
  - design-brief
  - template
---

# Sub-design Brief — [Theme or Section Name]

> Copy this file into the relevant folder, rename it `[name] - Design Brief.md`, and fill every section. Leave nothing implicit. The master brief is inherited and not repeated here.

Parent: [_Master Design Brief](_MASTER%20DESIGN%20BRIEF.md)

---

## 1. Theme statement and positioning

- **One-line theme:** _(e.g. "A portfolio read like a star chart: navigation by coordinates, not menus.")_
- **Metaphor:** _(what real-world system the design borrows from)_
- **Positioning:** _(how it should feel versus a generic portfolio)_
- **What success looks like:** _(one or two sentences)_

## 2. Glossary researched by the user

Terms used by this design, with sources and **why they matter here**. Definitions alone are not enough — write the rationale in prose.

| Term | Definition | Why it matters here | Source |
| --- | --- | --- | --- |
| _term_ | _short definition_ | _why this design uses it_ | _link_ |

Link shared terms to the [Glossary](Glossary.md) so there is one definition.

## 3. Color palette

### Tokens
| Token | Hex | RGB | Role | Contrast on bg |
| --- | --- | --- | --- | --- |
| color-bg |  |  |  |  |
| color-surface |  |  |  |  |
| color-text |  |  |  |  |
| color-text-muted |  |  |  |  |
| color-accent |  |  |  |  |
| color-accent-2 |  |  |  |  |
| color-border |  |  |  |  |
| color-focus |  |  |  |  |

Map each token to the global token names in the master brief.

### Combination examples
Show real pairings with usage notes and do/don't.

| Combination | Swatches | Where used | Do | Don't |
| --- | --- | --- | --- | --- |
| Background + text | `bg` / `text` | body copy | full-page reading | use for large display |
| Background + accent | `bg` / `accent` | primary CTA | single action focus | multiple competing accents |
| Surface + accent-2 | `surface` / `accent-2` | tags, data | short labels | long text |

Include at least one image or rendered swatch strip per combination in `assets/references/`.

## 4. Typography and iconography

- **Display face:** _(name, why, fallback)_
- **Body face:** _(name, why, fallback)_
- **Mono / data face:** _(name, why, fallback)_
- **Scale overrides:** _(only if the global scale is insufficient — log it)_
- **Iconography:** _(style, stroke weight, source, how it echoes the theme)_

## 5. Design ideas sourced from the glossary

Every idea must trace to a glossary term and, where possible, a reference image.

| # | Design idea | Glossary term(s) | Why it works | Reference image |
| --- | --- | --- | --- | --- |
| 1 |  |  |  | `assets/references/…` |
| 2 |  |  |  |  |

## 6. Imagery and art direction

- **Mood:** _(three to five adjectives)_
- **Subject matter:** _(what images are allowed)_
- **Treatment:** _(color grade, grain, crop, overlays)_
- **Sourcing rule:** _(e.g. public-domain NASA imagery only; copyrighted art reference-only, never shipped)_
- **Moodboard:** embed images from `assets/references/`.

## 7. Layout and component inventory

| Component | Reuses global? | Theme override |
| --- | --- | --- |
| Header / nav | yes / no |  |
| Card | yes / no |  |
| Button | yes / no |  |
| Tag | yes / no |  |
| Timeline | yes / no |  |

## 8. Page and section spec

For **each** page or section, fill the master brief's output contract:

### Section: [name]
- **Purpose:**
- **Content blocks:** _(block — content — priority)_
- **Visual hierarchy:** 1st / 2nd / 3rd
- **Layout:** desktop / tablet / mobile
- **Tokens used:**
- **States:** default / hover / focus / active / empty / loading / error
- **Motion:**
- **Accessibility:**
- **Open questions:**

## 9. Motion

| Element | Trigger | Duration | Easing | Reduced-motion fallback |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

## 10. Assets and references

| Asset | File | Source | License | Used in |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

## 11. Open questions and decisions

- Open questions: _(link to [Decision Log](Decision%20Log.md))_
- Decisions made: _(link to [Decision Log](Decision%20Log.md))_

## 12. Acceptance checklist

- [ ] Glossary has a source and rationale for every term used.
- [ ] Palette includes roles, contrast values, and combination examples.
- [ ] Every design idea cites a glossary term and/or reference image.
- [ ] Typography, iconography, and imagery direction are defined.
- [ ] Every section follows the output contract.
- [ ] All states and breakpoints are specified.
- [ ] Accessibility notes present.
- [ ] No code in the spec.
