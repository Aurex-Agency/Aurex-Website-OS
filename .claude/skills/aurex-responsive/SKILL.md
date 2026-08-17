---
name: aurex-responsive
description: Audits and redesigns responsive behavior so mobile, tablet, laptop, and large desktop experiences feel intentionally composed rather than mechanically stacked.
---

# Aurex Responsive Design

Responsive work is design, not cleanup.

Technically responsive is not creatively approved. On full website work, this skill runs as a dedicated mobile art-direction pass after desktop visual approval and before mobile visual approval or launch readiness.

## Review each major breakpoint for

- message hierarchy
- section order
- line length and type scale
- navigation model
- CTA visibility and sticky behavior
- imagery crop and focal point
- media aspect ratios
- content density
- grid behavior
- horizontal overflow
- tap targets
- form usability and keyboard behavior
- motion intensity
- interaction alternatives
- touch interactions and non-hover alternatives
- sticky storytelling-section entry, active states, progress, and exit
- proof visibility
- whitespace and pacing

## Mobile decisions

Ask whether the desktop composition should:

- stack
- reorder
- simplify
- crop differently
- replace an interaction
- reduce motion
- use a sticky conversion action
- shorten supporting copy
- change visual emphasis
- preserve a scroll-linked or sticky concept with mobile-specific choreography

Do not remove important proof or content merely to make mobile shorter.

Make image crop and focal-point decisions per viewport. Do not assume the desktop aspect ratio or `object-position` is acceptable on mobile.

Adapt motion to the viewport, input method, device performance, and `prefers-reduced-motion` without automatically deleting the signature experience. Preserve native scrolling and never introduce scroll-jacking.

## Breakpoints

Use breakpoints when the composition needs them, not because a framework ships preset names. Inspect meaningful widths around where the actual layout begins to fail.

## Browser QA

Use 390x844, 393x852, and a representative width around 430px as recommended review viewports. Test representative pages at all three when the work is visually significant, and resize through intermediate widths to catch breakpoints that screenshots alone miss. Inspect full-page and real scroll states, not only the page top.

For sticky or scroll-linked sections, verify the complete sequence: entry, active-state changes, image/content synchronization, progress indication, exit, CTA access, touch behavior, reduced-motion behavior, and recovery after orientation or viewport changes.

## Quality bar

The mobile site should feel like the same creative concept expressed for a different canvas, not a stripped-down emergency version of desktop.

Fix responsive problems before declaring visual QA complete. Record a distinct mobile visual verdict and stop for explicit human + ChatGPT approval before launch-readiness work.
