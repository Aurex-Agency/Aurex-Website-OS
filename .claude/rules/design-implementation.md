---
paths:
  - "**/*.{css,scss,ts,tsx,js,jsx}"
---

# Design Implementation Rules

- Implement the approved creative direction, not the defaults of Tailwind, shadcn, Radix, or the starter project.
- Encode repeated brand decisions as project-specific design tokens.
- Use Tailwind theme variables or CSS variables for colors, typography, spacing, radii, shadows, containers, and motion values when they represent system decisions.
- Do not let default Tailwind colors, default shadcn styling, or generic neutral palettes silently become the client's identity.
- Do not solve every section with `rounded-xl border bg-card p-6 shadow-sm` or equivalent card repetition.
- Do not default every page to centered heading + paragraph + three equal columns.
- Preserve intentional section rhythm by varying composition, scale, imagery, density, alignment, and surface treatment according to content.
- Use white backgrounds when strategically appropriate, not as an automatic canvas for every section.
- Treat imagery as part of composition. If the required asset is missing, preserve the concept with a labeled placeholder and document the needed shot rather than collapsing the design.
- Keep primary CTAs visually recognizable across the site while allowing context-specific supporting CTAs.
- Avoid excessive pills, badges, glass panels, gradients, shadows, rounded containers, and decorative grids unless the creative direction calls for them.
- Typography hierarchy should be obvious without relying on color alone.
- Responsive behavior may change composition, order, crop, alignment, and motion. Mobile is not a shrink pass.
- Before considering a section finished, ask whether it could be copied unchanged into an unrelated business. If yes, push the design closer to the approved concept.