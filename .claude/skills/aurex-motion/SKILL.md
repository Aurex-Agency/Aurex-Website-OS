---
name: aurex-motion
description: Creates a purposeful motion system for Aurex websites, including page entrance, scroll, hover, transitions, reduced motion, and performance-aware interaction.
---

# Aurex Motion

Motion should extend the creative concept, guide attention, create continuity, or improve feedback. It should not exist simply because animation is available.

## Establish the motion brief

Define:

- motion personality
- intensity from 1-10, usually 3-7
- signature motion moments
- standard entrance behavior
- section-transition behavior
- image/media behavior
- typography behavior
- hover/focus feedback
- navigation behavior
- scroll-linked behavior if justified
- mobile reductions or alternatives
- reduced-motion behavior

## Tool choice

Choose the simplest technology that can express the intended interaction well.

Prefer normal CSS transitions or the project's primary motion library for routine UI behavior. Reserve timeline-heavy or advanced scroll animation for signature moments that actually require it.

Do not add a new animation dependency for a trivial effect.

## Choreography

Use sequencing intentionally. Important elements may enter in relationship to one another, but avoid making the visitor wait for information.

Avoid uniform fade-up animation on every section.

## Concept connection

Ask whether motion can express something native to the business, such as focus, assembly, reveal, protection, transformation, movement, scale, precision, texture, or another approved concept.

Do not turn a metaphor into a repeated gimmick.

## Performance and accessibility

- respect `prefers-reduced-motion`
- avoid motion required to access content
- avoid expensive effects that cause visible jank
- test actual mobile behavior
- avoid scroll hijacking unless there is an exceptional, tested reason
- ensure hover-only information has accessible alternatives

## QA

Review motion in the running site at normal interaction speed. Ask:

- does it direct attention correctly?
- does it make the site feel more premium or merely busier?
- is anything delayed unnecessarily?
- does animation compete with CTA clarity?
- does the concept remain coherent across pages?
- is mobile calmer where needed?

Document the final motion system in `DESIGN-SYSTEM.md` or a dedicated `MOTION-SYSTEM.md` when complexity warrants it.
