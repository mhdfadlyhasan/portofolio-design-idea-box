---
title: "Reference - Arknights Endfield"
status: reference
version: 0.1
updated: 2026-11-14
type: visual-reference
used-by: "stellar map"
tags:
  - reference
  - moodboard
  - arknights
---

# Reference — Arknights: Endfield

A visual reference source, **not a theme** and not a subject to explain. Nothing here ships; it only informs the stellar map direction. Copyrighted art is reference-only and must never be embedded as a final asset.

[Back to master brief](../_MASTER%20DESIGN%20BRIEF.md) · [stellar map brief](../stellar%20map/stellar%20map%20-%20Design%20Brief.md)

---

## What it is

A sci-fi role-playing game by Hypergryph, known for an industrial-technical interface language. It is referenced here purely for UI and art-direction cues.

## Why it is referenced

Its interfaces show how dense technical information can stay calm and legible. That balance — instrument data without visual noise — is the same problem the stellar map theme has.

## Observed visual language

> Observations below are to be verified against actual screenshots in `assets/references/`. Treat as hypotheses until an image is attached.

- **Palette:** ash white, graphite and near-black, with a single hazard yellow / amber signal color.
- **Typography:** condensed or mono-style labels, ALL-CAPS micro-text, small tracking, data readouts.
- **Chrome:** hairline borders, corner ticks, crosshairs, measurement marks, grid overlays.
- **Density:** information-dense but spaced; hierarchy carried by size and color, not decoration.
- **Imagery:** industrial environments, matte surfaces, cold light, restrained effects.

## What to borrow for stellar map

- Hairline grid and corner-tick language for panels and section dividers.
- Mono micro-labels for coordinates, tags, and timestamps.
- One signal accent (amber) reserved for emphasis, never for large fills.
- Calm density: many small labels, few loud elements.

## What not to copy

- Its actual logos, characters, art, or UI screens — copyrighted, reference only.
- Hazard/industrial mood that would fight the calm, vast stellar tone.
- Excess UI chrome: the stellar map should feel like a map, not a game HUD.
- All-caps paragraphs; reserve caps for short labels only.

## Palette cues (to resolve into tokens)

| Cue | Approx. family | Use in stellar map |
| --- | --- | --- |
| Ash white | `#E8EEF7` | already `color-text` |
| Graphite | `#0B1220` | already `color-surface` |
| Hazard amber | `#F2B455` | already `color-accent-2` |
| Cold signal | cyan family | already `color-accent` |

The stellar map palette already absorbs these cues, so no new tokens are needed.

## Source table

| Reference | File | Source URL | License | Use |
| --- | --- | --- | --- | --- |
| UI screenshots | _to add_ | _to add_ | copyrighted — reference only | study layout and labels |
| Key art | _to add_ | _to add_ | copyrighted — reference only | mood only |
| Type specimens | _to add_ | _to add_ | _verify_ | label treatment |

## Rules

1. Never ship copyrighted Arknights assets.
2. Use it to justify a decision, then cite that decision in the [Decision Log](../Decision%20Log.md).
3. If a cue conflicts with accessibility or the stellar map mood, the stellar map wins.
