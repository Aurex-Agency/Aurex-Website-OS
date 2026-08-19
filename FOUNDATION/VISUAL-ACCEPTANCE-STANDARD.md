# Aurex Visual Acceptance Standard

Visual Acceptance is the creative approval decision for the rendered experience. It is separate from Technical QA.

Technical QA asks whether the site works reliably, safely, accessibly, and as specified. Visual Acceptance asks whether the running site expresses the approved direction with strong hierarchy, composition, rhythm, imagery, signature moments, responsive art direction, and perceived finish.

Neither can replace the other. A technically correct site may fail Visual Acceptance, and a beautiful site may fail Technical QA.

## Required evidence

Review the running experience, not source code alone. Inspect full pages and meaningful scroll states at representative desktop and mobile widths, plus intermediate widths where composition changes.

Judge in macro-before-micro order:

1. narrative, hierarchy, and conversion path
2. composition, scale, rhythm, density, and section transitions
3. imagery/media treatment and continuity
4. typography, color balance, contrast, and CTA prominence
5. execution of the approved 1-3 signature moments
6. mobile translation and responsive transitions
7. interaction details, component states, and fine polish

## Verdicts

- REJECT: concept or experience is materially off direction
- REVISE: major visual findings remain
- APPROVE WITH POLISH: direction is successful; only bounded non-blocking refinements remain
- APPROVE: no material visual findings remain

Record desktop and mobile verdicts separately against the reviewed commit or deployment. Desktop approval starts the dedicated mobile art-direction pass; it does not approve mobile. Launch readiness still requires the existing explicit human + ChatGPT mobile visual approval gate.

Use `/aurex-polish` before acceptance when the implementation needs refinement. Use `/aurex-visual-qa` to issue and record the acceptance verdict. Keep build, lint, tests, integrations, security, crawlability, and other system checks in `/aurex-technical-qa`.
