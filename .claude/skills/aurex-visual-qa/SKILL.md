---
name: aurex-visual-qa
description: Performs browser-based creative, UX, conversion, responsive, accessibility, and polish review of a running Aurex website and drives iterative fixes.
---

# Aurex Visual QA

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

## Iteration loop

1. inspect
2. document evidence
3. prioritize blockers and majors
4. fix
5. inspect again
6. compare against the approved concept and prior state

Do not declare visual completion with unresolved blockers. Desktop approval does not imply mobile approval.

For full website work, issue and record separate desktop and mobile verdicts. After the mobile pass, stop for explicit human + ChatGPT mobile visual approval. Do not recommend or begin launch readiness until that approval is recorded against the reviewed commit/deployment.

## Output

Maintain `QA-REPORT.md` with scores, screenshots/observations where available, prioritized fixes, resolved findings, remaining risks, and final recommendation: REJECT / REVISE / APPROVE WITH POLISH / APPROVE.
