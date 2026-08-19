---
name: aurex-motion
description: Directs and implements a purposeful Aurex motion system, using Motion as the default premium React animation layer while keeping creative judgment, tool choice, reduced motion, and performance proportional to the approved concept.
---

# Aurex Motion

Motion should extend the creative concept, guide attention, create continuity, or improve feedback. It should not exist simply because animation is available.

Read `references/MOTION-AI-TOOLING.md` before using Motion AI Kit. Aurex owns creative judgment; use Motion's current AI tooling and official documentation for API syntax, implementation patterns, performance guidance, and reduced-motion practices.

## Establish the motion brief

Define:

- motion personality
- intensity from 1-10, usually 3-7
- which of the approved 1-3 signature moments use motion, and why
- standard entrance behavior
- section-transition behavior
- image/media behavior
- typography behavior
- hover/focus feedback
- navigation behavior
- scroll-linked behavior if justified
- mobile reductions or alternatives
- mobile-specific sticky/scroll choreography and touch behavior
- reduced-motion behavior

## Tool choice

Choose the simplest technology that can express the intended interaction well.

- Native CSS: simple transitions, hover/focus states, and self-contained effects. Motion AI Kit may generate CSS `linear()` spring easing without adding a runtime.
- Motion: default premium layer for most React animation, layout transitions, gestures, entrance choreography, shared-element effects, and reasonable scroll-triggered or scroll-linked effects.
- GSAP/ScrollTrigger: only for complex timelines, pinned storytelling, advanced scroll choreography, or an experience that genuinely justifies it.
- Rive: optional for custom branded interactive graphics, diagrams, animated marks, and state-driven illustrations.
- Three.js / React Three Fiber: only when the approved creative concept genuinely benefits from 3D.

Do not add GSAP, Rive, Three.js, React Three Fiber, Aceternity, or another heavy dependency to a starter or client project by default. Introduce an optional tool only after the approved concept names the need, simpler tools are insufficient, and its performance/accessibility cost is accepted. Do not add a new animation dependency for a trivial effect.

Motion AI Kit is development-environment tooling. Prefer a global Claude Code installation. Do not add its MCP configuration, agent skill, or SDK to client projects. Install the `motion` runtime in a client only when the implementation uses it, following current official documentation and the client's package manager.

## Choreography

Use sequencing intentionally. Important elements may enter in relationship to one another, but avoid making the visitor wait for information.

Avoid generic AI animation. Do not default sections to repeated opacity + `translateY` fade-ups, uniform stagger recipes, or copied demo effects. Every material animation must reinforce hierarchy, continuity, interaction feedback, storytelling, or the approved signature concept. Static is better than unjustified motion.

## Concept connection

Ask whether motion can express something native to the business, such as focus, assembly, reveal, protection, transformation, movement, scale, precision, texture, or another approved concept.

Do not turn a metaphor into a repeated gimmick.

## Performance and accessibility

- respect `prefers-reduced-motion`
- when Motion is used, apply the current official reduced-motion APIs and choose a site-wide policy deliberately; use bespoke alternatives for parallax, autoplay, and other motion-sensitive behavior
- avoid motion required to access content
- avoid expensive effects that cause visible jank
- test actual mobile behavior at 390x844, 393x852, and a representative width around 430px when motion is visually significant
- avoid scroll hijacking unless there is an exceptional, tested reason
- ensure hover-only information has accessible alternatives

Do not automatically replace a signature desktop scroll scene with a static stack on mobile. Preserve the same narrative purpose with viewport-specific choreography when it remains accessible, performant, touch-appropriate, and compatible with native scrolling. Verify sticky entry, progress, active-state/image synchronization, exit, CTA access, and reduced-motion behavior through the full sequence.

## QA

Review motion in the running site at normal interaction speed. Ask:

- does it direct attention correctly?
- does it make the site feel more premium or merely busier?
- is anything delayed unnecessarily?
- does animation compete with CTA clarity?
- does the concept remain coherent across pages?
- is mobile calmer where needed?
- did Motion strengthen one of the intended 1-3 signature moments or merely decorate the page?

When Motion AI Kit is available, use its current docs before relying on remembered syntax. Use MotionScore when available and proportionate, but verify the running site in the browser regardless. Feed motion findings into `/aurex-polish` and Visual Acceptance in macro-before-micro order; do not create a separate motion approval bureaucracy.

Document the final motion system in `DESIGN-SYSTEM.md` or a dedicated `MOTION-SYSTEM.md` when complexity warrants it.
