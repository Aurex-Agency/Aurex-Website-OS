---
paths:
  - "**/*.{ts,tsx,js,jsx,css,scss}"
---

# Motion Engineering Rules

- Motion must extend the approved creative concept or improve feedback, hierarchy, continuity, or storytelling.
- Use CSS transitions for simple hover/focus/state changes when they are sufficient.
- Use Motion for most React animation, layout transitions, gestures, ordinary reveals, and ordinary scroll-linked effects.
- Use GSAP/ScrollTrigger only when the concept requires capabilities such as coordinated timelines, pinning, scrubbing, advanced parallax, SVG choreography, or complex scroll-state orchestration.
- Do not install or mix animation libraries without a clear division of responsibility.
- Do not apply the same fade-up reveal to every section.
- Avoid hiding meaningful content for long entrance sequences.
- Do not make users wait for animation before they can read or convert.
- Prefer transform and opacity for high-frequency movement. Avoid layout-thrashing animation.
- Clean up observers, event listeners, Motion subscriptions, GSAP timelines, and ScrollTriggers on unmount.
- Verify scroll-trigger calculations after responsive layout changes and image loading.
- Never globally apply `will-change` as a performance superstition.
- Respect `prefers-reduced-motion`. Complex motion must degrade to an immediate, readable, fully usable state.
- Reduce or remove expensive motion on mobile when the value does not justify the cost.
- Scroll hijacking is not an Aurex default.
- If the animation is the most memorable thing on the page but the business promise is not, the motion is too dominant.