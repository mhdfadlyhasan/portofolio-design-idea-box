---
title: Master Design Brief
status: draft
version: 0.1
updated: 2026-11-14
active-theme: stellar map
output: design-spec-only
tags:
  - design-brief
  - master
  - portfolio
---

# Master Design Brief

The governing document for this portfolio. Every design session — human or AI — starts here, then loads the active theme brief.

- Active theme: [stellar map](stellar%20map/stellar%20map%20-%20Design%20Brief.md)
- Reference library: [Arknights Endfield reference](Arknights%20endfield/Reference%20-%20Arknights%20Endfield.md)
- Shared vocabulary: [Glossary](Glossary.md)
- Decisions and open questions: [Decision Log](Decision%20Log.md)
- Images and moodboard: [`assets/references/`](assets/references/)

---

## 0. How to use this document

### Reading order (for an AI session)
1. This file, end to end.
2. [`Glossary.md`](Glossary.md) — all vocabulary is defined there.
3. The active theme brief ([stellar map](stellar%20map/stellar%20map%20-%20Design%20Brief.md)).
4. [`Decision Log.md`](Decision%20Log.md) — respect prior decisions; do not reopen them silently.
5. Reference note(s) only when a theme brief points to them.

### AI output contract
The deliverable is a **design spec only**. No HTML, CSS, JS, or framework code.

For every page or section, produce in this order:
1. **Purpose** — what it is for, in one sentence.
2. **Content blocks** — each block, its content, and priority (must / should / nice).
3. **Visual hierarchy** — what the eye reads first, second, third.
4. **Layout** — grid, columns, alignment, spacing, and what changes at each breakpoint.
5. **Tokens used** — reference named tokens from the global design system only.
6. **States** — default, hover, focus, active, empty, loading, error.
7. **Motion** — trigger, duration, easing, reduced-motion fallback.
8. **Accessibility notes** — contrast, focus order, alt text.
9. **Open questions** — anything not yet decided.

Rules:
- Do not invent colors, type sizes, spacing, or terminology. Use the tokens and glossary terms defined here.
- Every design idea must cite its source: a glossary term and/or a reference image.
- If a decision is missing, propose an option and add it to the [Decision Log](Decision%20Log.md) rather than assuming.
- Prefer plain, portable markdown. Standard relative links only; no Obsidian Canvas or Dataview.

---

## 1. Project overview

| Field | Value |
| --- | --- |
| Subject | Personal portfolio |
| Active theme | stellar map |
| Primary goal | Show who I am and what I build, then drive contact |
| Audience | _(to fill)_ recruiters, collaborators, clients, peers |
| Success criteria | _(to fill)_ e.g. a visitor understands my focus within 10 seconds and can reach contact in two clicks |
| Non-goals | _(to fill)_ e.g. no blog, no CMS, no login |
| Tone of voice | Calm, precise, exploratory — like a mission log, not a sales pitch |

## 2. Information architecture

Landing page plus everything else inside the stellar map theme.

```
/                  Home (single scrolling narrative + section anchors)
/#work             Selected work
/#about            About
/#capabilities     Skills / capabilities
/#process          Process
/#experience       Experience
/#contact          Contact
```

- Navigation: header with section anchors, persistent on scroll.
- Footer: contact, socials, back-to-top.
- URL/section map to be confirmed later (see [Decision Log](Decision%20Log.md)).

## 3. Main page — information to show

Scaffold only. Content is seeded later; an AI may propose, but must mark proposals.

| # | Block | Purpose | Priority | Content source | CTA |
| --- | --- | --- | --- | --- | --- |
| 1 | Hero | State who I am and what I do | must | _to fill_ | View work |
| 2 | Positioning line | One sentence that frames the work | must | _to fill_ | — |
| 3 | Selected work | Proof, three to five projects | must | _to fill_ | Open project |
| 4 | About | Context and point of view | should | _to fill_ | — |
| 5 | Capabilities | What I can do | should | _to fill_ | — |
| 6 | Process | How I work | nice | _to fill_ | — |
| 7 | Experience | Timeline / credibility | should | _to fill_ | — |
| 8 | Contact | Convert interest into a message | must | _to fill_ | Email / socials |

## 4. Main page — information flow

Scaffold only. Proposed narrative: **hook → who → proof → depth → action**.

1. **Hook (above the fold):** name, role, one-line positioning, primary CTA. No scrolling required to understand the site.
2. **Who:** a short orientation before proof, so work is read in context.
3. **Proof:** selected work, strongest first; each tile leads to detail or expands inline.
4. **Depth:** capabilities, process, experience.
5. **Action:** contact and socials, repeated in footer.

Rules:
- Never place more than one competing primary CTA in view.
- Each section should stand alone but link forward naturally.
- State all interactive states (see section 0 output contract).
- Define behavior for empty, loading, and error where content is dynamic.

## 5. Global design system

Inherited by every theme and section. Themes may override only with logged decisions.

### Grid and spacing
- Base unit: 4px.
- Spacing scale: 4, 8, 12, 16, 24, 32, 48, 64, 96, 128.
- Container: max-width 1200px, gutter 24px (16px on small screens).
- Grid: 12 columns desktop, 8 tablet, 4 mobile.

### Breakpoints
| Name | Min width |
| --- | --- |
| mobile | 0 |
| tablet | 768px |
| desktop | 1200px |

### Typography scale
| Token | Size / line | Use |
| --- | --- | --- |
| type-display | 64 / 1.05 | hero |
| type-h1 | 40 / 1.15 | section titles |
| type-h2 | 28 / 1.25 | block titles |
| type-body | 17 / 1.6 | default text |
| type-small | 14 / 1.5 | meta, captions |
| type-mono | 13 / 1.4 | labels, data, coordinates |

### Color tokens
Global defaults live here; the theme brief defines the actual palette per token name.

| Token | Role |
| --- | --- |
| color-bg | page background |
| color-surface | cards, panels |
| color-text | primary text |
| color-text-muted | secondary text |
| color-accent | primary action / highlight |
| color-accent-2 | secondary highlight |
| color-border | dividers, outlines |
| color-focus | focus ring |
| color-success / warning / error | status |

### Other tokens
- Radius: none (0), sm (4), md (8), pill (999).
- Elevation: flat (border only), raised (soft shadow). Keep shadows minimal.
- Motion: fast 120ms, base 240ms, slow 480ms; easing `ease-out` for entering, `ease-in` for leaving.

## 6. Layout and component inventory

Global components every theme reuses:
- Header / nav (sticky, anchor links)
- Footer
- Button (primary / secondary / ghost)
- Card (work tile, capability)
- Tag / chip
- Timeline item
- Section wrapper (title + optional lede + content)
- Link (inline, with focus state)

## 7. Motion and interaction principles

- Motion communicates state, not decoration.
- Enter with `ease-out`, exit with `ease-in`.
- Respect `prefers-reduced-motion`: replace movement with simple fades.
- No motion may block reading or delay interaction.
- Hover states must be obvious and reversible.

## 8. Accessibility and performance

- Text contrast: minimum 4.5:1, large text 3:1.
- Visible focus ring on every interactive element; never remove focus styles.
- Full keyboard operation; logical focus order.
- Alt text for all meaningful images; decorative images marked empty.
- Target: Lighthouse accessibility 95+, performance 90+.
- Image budget: lazy-load below the fold; serve appropriately sized assets.

## 9. Content and copy guidelines

- Voice: calm, precise, first person, no hype.
- Sentences short; one idea per sentence.
- Headline length: aim under 10 words.
- Body paragraph: under 60 words where possible.
- Capitalization: sentence case for headings and buttons.
- Real copy only — placeholder text must be labeled `[placeholder]`.

## 10. Glossary and reference library

- All terms: [Glossary](Glossary.md).
- Visual references and images: [`assets/references/`](assets/references/).
- Theme-specific references: [stellar map brief](stellar%20map/stellar%20map%20-%20Design%20Brief.md).
- Secondary visual reference (not a theme): [Arknights Endfield](Arknights%20endfield/Reference%20-%20Arknights%20Endfield.md).

## 11. Decisions and definition of done

- Record decisions and open questions in the [Decision Log](Decision%20Log.md).
- A design spec is **done** when:
  - [ ] Every page/section follows the output contract in section 0.
  - [ ] Only named tokens are used; no ad-hoc values.
  - [ ] Every idea cites a glossary term and/or reference image.
  - [ ] All component states are specified.
  - [ ] Responsive behavior is defined at all three breakpoints.
  - [ ] Accessibility notes are present.
  - [ ] Open questions are logged.
  - [ ] It contains no code.

## 12. Versioning

| Version | Date | Change |
| --- | --- | --- |
| 0.1 | 2026-11-14 | Initial master brief created |
