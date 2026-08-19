---
name: aurex-visual-qa
description: Issues browser-based Visual Acceptance verdicts for a running Aurex website, separate from technical QA, after bounded refinement is complete.
---

# Aurex Visual QA

Read `FOUNDATION/VISUAL-ACCEPTANCE-STANDARD.md`. This skill owns the creative acceptance verdict. It does not duplicate build, lint, security, integration, crawlability, or other Technical QA checks.

Do not review a frontend only from source code. Inspect the running experience whenever browser tools are available.

## Review representative pages

At minimum inspect:

- homepage
- one key service/product page
- one trust/proof page when present
- primary conversion flow
- one complex page pattern

First establish the desktop visual verdict. After desktop approval, run a distinct mobile art-direction review at 390x844, 393x852, and a representative width around 430px, plus intermediate widths where layout behavior changes.

Technically responsive is not a mobile creative verdict. Inspect full pages and meaningful scroll states for composition, crop/focal point, hierarchy, density, CTA usability, touch behavior, motion adaptation, and sticky-section choreography. Verify accessibility, performance, native scrolling, and reduced-motion behavior; scroll-jacking is not acceptable.

## Scorecard

Review macro before micro: narrative/hierarchy and conversion path; composition/scale/rhythm; imagery; typography/color; signature moments; responsive translation; then component details and polish.

Score each area from 1-10 with evidence:

1. business/message clarity
2. conversion clarity
3. brand specificity
4. creative concept execution
5. visual hierarchy
6. typography
7. color and contrast
8. imagery/media
9. composition and section rhythm
10. motion and interaction
11. mobile quality
12. form/conversion experience
13. trust and proof
14. accessibility/usability
15. perceived performance and polish

Explicitly verify whether the approved 1-3 signature moments are present, purposeful, coherent, and successfully translated to mobile and reduced motion.

A numeric score without specific observations is not useful.

## AI/template detection

Flag:

- repeated card-grid solutions
- endless white sections
- generic centered hero patterns
- arbitrary gradients
- default component-library appearance
- excessive pills/badges
- repeated heading/paragraph/button section shapes
- generic stock imagery
- animation repeated without narrative purpose
- copy that could belong to another company
- suspiciously uniform spacing or composition

## Severity

Classify findings:

- BLOCKER: materially harms conversion, usability, accessibility, correctness, or brand direction
- MAJOR: makes the work feel generic, unfinished, inconsistent, or strategically weak
- POLISH: worthwhile refinement that does not block approval

## Acceptance loop

1. inspect the rendered experience
2. document evidence in macro-before-micro order
3. compare against the approved concept, signature moments, and prior state
4. issue the verdict

If fixes are needed, route the bounded refinement through `/aurex-polish`, then re-run Visual Acceptance. Do not create an unlimited QA/fix loop. Do not declare visual completion with unresolved blockers. Desktop approval does not imply mobile approval.

For full website work, issue and record separate desktop and mobile verdicts. After the mobile pass, stop for explicit human + ChatGPT mobile visual approval. Do not recommend or begin launch readiness until that approval is recorded against the reviewed commit/deployment.

## Output

Maintain `QA-REPORT.md` with scores, screenshots/observations where available, prioritized fixes, resolved findings, remaining risks, and final recommendation: REJECT / REVISE / APPROVE WITH POLISH / APPROVE.
