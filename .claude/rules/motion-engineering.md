---
paths:
  - "**/*.{ts,tsx,js,jsx,css,scss}"
---

# Motion Engineering Rules

- Motion must extend the approved creative concept or improve feedback, hierarchy, continuity, or storytelling.
- Use native CSS for simple transitions, hover/focus states, and self-contained effects.
- Use Motion as the default premium implementation layer for most React animation, layout transitions, gestures, entrance choreography, shared-element effects, and reasonable scroll-triggered or scroll-linked effects.
- Use current Motion documentation or Motion AI Kit for syntax and implementation guidance instead of relying on remembered `framer-motion` APIs. Current React imports come from `motion/react`.
- Use GSAP/ScrollTrigger only for complex timelines, pinned storytelling, advanced scroll choreography, or experiences that genuinely justify it.
- Use Rive only for approved custom branded interactive graphics, diagrams, animated marks, or state-driven illustrations.
- Use Three.js / React Three Fiber only when the approved concept genuinely benefits from 3D.
- Do not add GSAP, Rive, Three.js, React Three Fiber, Aceternity, or other heavy animation/UI dependencies by default.
- Do not install or mix animation libraries without a clear division of responsibility.
- Guard against generic AI animation: do not apply repeated opacity + translateY fade-ups, uniform staggers, or copied demo effects across sections.
- Every material animation must reinforce hierarchy, continuity, interaction, storytelling, or one of the approved 1-3 signature moments.
- Avoid hiding meaningful content for long entrance sequences.
- Do not make users wait for animation before they can read or convert.
- Prefer transform and opacity for high-frequency movement. Avoid layout-thrashing animation.
- Clean up observers, event listeners, Motion subscriptions, GSAP timelines, and ScrollTriggers on unmount.
- Verify scroll-trigger calculations after responsive layout changes and image loading.
- Never globally apply `will-change` as a performance superstition.
- Respect `prefers-reduced-motion`. When Motion is used, follow its current official `MotionConfig`/`useReducedMotion` guidance and provide deliberate alternatives for parallax, autoplay, large transforms, and other motion-sensitive behavior. Complex motion must degrade to an immediate, readable, fully usable state.
- Reduce or remove expensive motion on mobile when the value does not justify the cost.
- Scroll hijacking is not an Aurex default.
- If the animation is the most memorable thing on the page but the business promise is not, the motion is too dominant.
