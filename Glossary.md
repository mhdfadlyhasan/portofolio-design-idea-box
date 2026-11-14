---
title: Glossary
status: living
version: 0.1
updated: 2026-11-14
tags:
  - glossary
  - vocabulary
---

# Glossary

Shared vocabulary for this portfolio. Every term used in a brief must be defined here or in a theme brief, with a source and **why it matters**. Definitions alone are not enough: the "why" column explains the design consequence.

> Seed set. Verify each source and extend as the design grows. Keep one definition per term here; theme briefs link back to it.

[Back to master brief](_MASTER%20DESIGN%20BRIEF.md) · [Decision Log](Decision%20Log.md)

---

## Domain terms — stellar map

| Term | Definition | Why it matters here | Source |
| --- | --- | --- | --- |
| Cartography | The study and practice of making maps. | Frames the whole site as a map to be read, not a brochure to be skimmed. Drives layout, labels, and navigation. | [Wikipedia](https://en.wikipedia.org/wiki/Cartography) |
| Celestial sphere | An imaginary sphere around the Earth on which celestial bodies are projected. | Justifies a full-viewport, curved-space feel; content can sit on a spherical coordinate grid rather than a flat list. | [Wikipedia](https://en.wikipedia.org/wiki/Celestial_sphere) |
| Equatorial coordinate system | A celestial coordinate system using right ascension and declination. | Gives us a naming model for section anchors and data labels (e.g. two-part coordinates) instead of generic numbers. | [Wikipedia](https://en.wikipedia.org/wiki/Equatorial_coordinate_system) |
| Right ascension / declination | The two angles that locate a point on the celestial sphere. | Encodes hierarchy: one axis for section, one for item. Useful for tag and anchor notation. | [Wikipedia](https://en.wikipedia.org/wiki/Equatorial_coordinate_system) |
| Horizontal coordinate system | Locates objects by altitude and azimuth relative to the observer. | Reminds us the map is seen from a viewer's position; supports "you are here" orientation cues. | [Wikipedia](https://en.wikipedia.org/wiki/Horizontal_coordinate_system) |
| Star chart | A map of celestial bodies used for navigation and study. | The core visual metaphor: constellation lines, node labels, and plotted points for projects. | [Wikipedia](https://en.wikipedia.org/wiki/Star_chart) |
| Constellation | A recognized grouping of stars. | Model for grouping related work or skills into named clusters instead of flat grids. | [Wikipedia](https://en.wikipedia.org/wiki/Constellation) |
| Astrolabe | An ancient instrument for locating and predicting celestial positions. | Reference for instrument-like UI chrome: rings, scales, crosshairs, precision marks. | [Wikipedia](https://en.wikipedia.org/wiki/Astrolabe) |
| Parallax | Apparent shift in position when viewed from different points. | Justifies subtle depth on scroll (background layers move slower); must degrade for reduced motion. | [Wikipedia](https://en.wikipedia.org/wiki/Parallax) |
| Ephemeris | A table of predicted positions of celestial bodies over time. | Model for the experience/timeline section: dated rows like an almanac rather than a generic list. | [Wikipedia](https://en.wikipedia.org/wiki/Ephemeris) |
| Sidereal time | Time measured by the Earth's rotation relative to the stars. | A quiet detail for labels and loading states; use sparingly, never as required information. | [Wikipedia](https://en.wikipedia.org/wiki/Sidereal_time) |
| Nautical almanac | A yearly publication of celestial navigation data. | Reference for data-dense but legible tables; keeps numbers feeling purposeful, not decorative. | [Wikipedia](https://en.wikipedia.org/wiki/Nautical_almanac) |
| Wayfinding | Systems that help people orient and navigate a space. | The actual job of the site's nav: orientation and next step, not just links. | [Wikipedia](https://en.wikipedia.org/wiki/Wayfinding) |
| Beacon | A fixed signal used as a navigational reference. | Model for the primary CTA and contact: one steady, always-findable signal. | [Wikipedia](https://en.wikipedia.org/wiki/Beacon) |
| Orbit | A curved path around a central body. | Optional layout metaphor for secondary content circling a central idea; avoid if it costs readability. | [Wikipedia](https://en.wikipedia.org/wiki/Orbit) |
| HUD (heads-up display) | A transparent display presenting data without requiring the viewer to look away. | Reference for overlay labels and persistent status elements; keep contrast and legibility above atmosphere. | [Wikipedia](https://en.wikipedia.org/wiki/Head-up_display) |
| Telemetry | Automated measurement and transmission of data from a remote source. | Reference for live-feeling micro-data (status text, counters); must not fake data or mislead. | [Wikipedia](https://en.wikipedia.org/wiki/Telemetry) |

## Design terms

| Term | Definition | Why it matters here | Source |
| --- | --- | --- | --- |
| Information architecture | The structural design of shared information environments. | Decides section order and grouping; the master brief's section 2 and 4 depend on it. | [Wikipedia](https://en.wikipedia.org/wiki/Information_architecture) |
| Visual hierarchy | Arranging elements so the eye reads them in a chosen order. | Every section spec must state first/second/third; prevents flat, undirected pages. | [Wikipedia](https://en.wikipedia.org/wiki/Visual_hierarchy) |
| Design token | A named, reusable value for color, type, spacing, etc. | Lets the AI reference `color-accent` instead of a hex, keeping themes consistent. | [Wikipedia](https://en.wikipedia.org/wiki/Design_token) |
| Design system | A reusable set of components and standards. | The master brief's global system; themes override only with a logged decision. | [Wikipedia](https://en.wikipedia.org/wiki/Design_system) |
| Moodboard | A collection of reference images expressing a direction. | Anchors the stellar map look in concrete images instead of adjectives. | [Wikipedia](https://en.wikipedia.org/wiki/Mood_board) |
| Wireframe | A low-fidelity layout sketch. | Optional intermediate step between spec and final design; not a substitute for the spec. | [Wikipedia](https://en.wikipedia.org/wiki/Website_wireframe) |
| Breakpoint | A width at which a layout changes. | Forces explicit responsive behavior at mobile/tablet/desktop. | [Wikipedia](https://en.wikipedia.org/wiki/Responsive_web_design) |
| Contrast ratio | Luminance ratio between two colors. | Gates accessibility; palette combinations must state their ratios. | [W3C WCAG](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html) |
| Glossary | An alphabetical list of terms with definitions. | Prevents the AI and the designer from meaning different things by the same word. | [Wikipedia](https://en.wikipedia.org/wiki/Glossary) |
| Design specification | A written description of a design detailed enough to build from. | The sole deliverable of an AI session; no code. | [Wikipedia](https://en.wikipedia.org/wiki/Design_specification) |
