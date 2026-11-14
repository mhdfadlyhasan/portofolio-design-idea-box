---
title: Decision Log
status: living
version: 0.1
updated: 2026-11-14
tags:
  - decisions
  - log
---

# Decision Log

Append-only. Do not rewrite history: add a new row and mark an old decision `superseded` if it changes. An AI session must read this before proposing changes.

[Back to master brief](_MASTER%20DESIGN%20BRIEF.md) · [Glossary](Glossary.md)

## Decisions

| Date | Decision | Rationale | Status |
| --- | --- | --- | --- |
| 2026-11-14 | Active theme is **stellar map**. | Chosen over the alternate exploration; landing page and all sections live in this theme. | accepted |
| 2026-11-14 | Arknights Endfield is a **visual reference only**, not a theme or a subject to explain. | Source of aesthetic cues; not a section of the portfolio. | accepted |
| 2026-11-14 | Deliverable of an AI design session is a **design spec only**, no code. | Keeps sessions focused on decisions and structure before implementation. | accepted |
| 2026-11-14 | `_MASTER DESIGN BRIEF.md` lives at the vault root. | Governs all themes; root keeps it visible and canonical. | accepted |
| 2026-11-14 | Use **plain, portable markdown**: standard relative links, no wikilinks, no Canvas/Dataview. | Same docs must render in Obsidian, VS Code, GitHub, and read cleanly for AI tools. | accepted |
| 2026-11-14 | Obsidian is a **viewer/editor**, not a dependency. | Files stay plain markdown; no lock-in. | accepted |
| 2026-11-14 | Main-page content blocks are scaffolded now, **seeded later**. | Structure first; real copy comes after the system is agreed. | accepted |

## Open questions

| # | Question | Owner | Status |
| --- | --- | --- | --- |
| 1 | Exact font choices for display, body, and mono. | _you_ | open |
| 2 | Final palette hex values and contrast ratios. | _you_ | open |
| 3 | Project list: how many, which ones, order. | _you_ | open |
| 4 | Whether selected work opens as sub-pages or expands inline. | _you_ | open |
| 5 | Hosting and framework (implementation phase only). | _you_ | open |
