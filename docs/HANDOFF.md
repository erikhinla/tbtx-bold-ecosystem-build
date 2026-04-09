# Production Handoff: Static TBTX Ecosystem

## Overview
This document guides the maintenance and extension of the **Static TBTX Ecosystem**. This version uses Vanilla JavaScript for all application logic to ensure zero-dependency portability.

## Logic Implementation: 15-Question Engine
The brain of the diagnostic system is located in:
`bizbotmarketing/index.html`

### Scoring Mechanism
- Every answer applies weighted points (0-3) to one or more of the 4 archetypes defined in the `intakeConfig` array.
- **Archetypes**: `toolOverload`, `bottleneckOperator`, `fragmentedWorkflow`, `executionStall`.
- At the end of the 15-question set, the script identifies the top-scoring archetype and routes to:
  `blueprint.html?archetype=[dominant_archetype]`

### Final State UX
The diagnostic was updated to prioritize action:
- **Primary CTA**: "→ BUILD THE SYSTEM" (Links to `/bizbuilders/index.html`)
- **Secondary Link**: "View Blueprint" (Links to results)

## Design System
The "Swiss Industrial Paint" aesthetic is derived from variables in `styles.css`.
- **Macro-Typography**: Uses `Archivo Black`.
- **Mechanical Grain**: SVG noise filter applied globally to body.
- **Zero Radius**: All borders must have `0 !important`.

## Deployment
This project is suitable for any static hosting environment.
1. Push to GitHub.
2. Link to Netlify or enable GitHub Pages.
3. No build steps are required.

---

Handed off by Antigravity.
