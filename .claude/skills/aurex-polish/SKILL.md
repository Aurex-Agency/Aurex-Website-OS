---
name: aurex-polish
description: Runs a browser-first visual refinement loop with no more than two bounded passes, fixing macro composition before micro polish. Use after a page or representative page pattern is implemented and technically runnable.
---

# Aurex Polish

Use this skill to improve a working implementation, not to reopen strategy or create a new design direction.

## Preconditions

- the relevant route runs in a browser
- the approved creative direction and page purpose are available
- the current implementation is complete enough to judge as a whole

If one of these is missing, name the blocker and return to the appropriate implementation step.

## Browser-first rule

Inspect the rendered page before reading deeply into components or proposing fixes. Review the full scroll experience at a representative desktop width first, then at the mobile viewports required by the current project. Use source inspection only to understand and implement observed problems.

Capture a concise baseline: the three highest-impact visual problems, the strongest element to preserve, and whether the approved 1-3 signature moments are present and working.

## Review order: macro before micro

Never spend the first pass tuning shadows, radii, icon offsets, or isolated spacing while larger composition problems remain.

Review in this order:

1. page narrative, hierarchy, and conversion path
2. section composition, scale, rhythm, density, and transitions
3. imagery/media choice, crop, focal point, and visual continuity
4. typography system, color balance, contrast, and CTA prominence
5. signature moments and motion/interaction purpose
6. responsive translation and intermediate-width behavior
7. component consistency, states, spacing, borders, shadows, and other fine detail

## Pass 1: structural refinement

Choose only the highest-impact macro findings, normally three to five. Fix composition, hierarchy, rhythm, media treatment, conversion clarity, and failed signature moments. Do not broaden scope into discovery, new page creation, or a full technical audit.

Reinspect the same routes and viewports after the changes.

## Pass 2: finishing refinement

Choose only the remaining changes that materially improve cohesion and perceived quality, normally three to five. Resolve typography, color balance, responsive details, interaction timing, states, and fine visual consistency.

Reinspect once more. Stop after this pass.

If a major visual problem remains, report it as a Visual Acceptance finding with a recommended next action. Do not start an unbounded third polish pass or silently redesign the concept.

## Boundaries

- Maximum: two implementation-and-reinspection passes per invocation.
- Preserve working, distinctive elements; do not churn the whole page for novelty.
- Do not use a specialist by default. Escalate only a specific unresolved creative decision.
- Do not substitute this skill for technical QA, accessibility verification, or the explicit mobile approval gate.
- A successful polish loop makes the work ready for Visual Acceptance; it does not grant approval itself.

## Output

Report:

- baseline and element preserved
- pass 1 changes and browser evidence
- pass 2 changes and browser evidence
- signature-moment status
- remaining Visual Acceptance findings
- ready / not ready for Visual Acceptance
