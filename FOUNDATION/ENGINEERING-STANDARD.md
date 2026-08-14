# Aurex Engineering Standard

This standard defines how Aurex turns approved strategy and creative direction into production websites without sacrificing originality, conversion, accessibility, organic visibility, or maintainability.

## 1. Default stack

For new Aurex marketing websites, the default stack is:

- Next.js App Router
- TypeScript
- Tailwind CSS
- React Server Components by default
- client components only where interactivity requires them
- Motion for most interface and scroll animation
- GSAP with ScrollTrigger only for interactions that genuinely need timeline, pinning, scrubbing, or advanced scroll choreography
- Radix or shadcn primitives when they save accessibility or interaction work, with fully custom visual styling
- Vercel as the default deployment target unless client constraints require another platform

The default stack is a starting point, not a religion. Preserve an existing stack when migration cost exceeds the benefit. Choose another framework only when project requirements materially justify it.

## 2. Architecture follows the website, not the starter template

Do not begin from a visually opinionated starter.

Aurex may standardize infrastructure, utilities, testing, analytics, accessibility patterns, and development conventions. It should not standardize the finished aesthetic.

The project architecture should support:

- multi-page information architecture
- server-rendered or pre-rendered crawlable content
- reusable underlying primitives
- page-specific compositions
- independent media strategies
- forms and integrations
- analytics and conversion measurement
- efficient responsive behavior
- accessible interactions

Reusable components should reduce engineering duplication without forcing visual sameness.

## 3. Server-first rendering

Prefer server-rendered content for static and content-heavy page regions.

Use client components only for behavior that requires browser state, browser APIs, animation, gesture handling, or interactive state.

Do not mark entire pages or large layout trees as client components simply because one child needs interaction.

Keep the client boundary as low and narrow as practical.

Benefits include less shipped JavaScript, stronger initial rendering, simpler SEO, and fewer hydration-related failure modes.

## 4. TypeScript standard

Use TypeScript for new projects.

Avoid `any` unless a boundary genuinely cannot be typed and the reason is documented.

Model important business concepts explicitly, especially:

- forms
- CMS data
- navigation
- locations
- services
- products
- testimonials
- case studies
- analytics events

Runtime data entering the system from forms, APIs, CMSs, URL parameters, or third parties must be validated at the boundary when correctness or security depends on it.

## 5. Tailwind is an implementation tool, not the design system

Aurex design systems should be encoded through project-specific tokens.

Use Tailwind theme variables and CSS variables to define client-specific:

- colors
- typography
- spacing
- radii
- shadows
- breakpoints when justified
- motion easings
- animation durations
- containers

Do not let Tailwind defaults silently become the brand.

Avoid arbitrary-value sprawl when a value represents a repeatable design decision. Promote repeated decisions into tokens.

## 6. Component libraries do not define the visual language

shadcn, Radix, and similar libraries may provide useful accessible primitives.

They must not determine the final Aurex aesthetic.

Do not leave default-looking:

- cards
- buttons
- accordions
- dialogs
- navigation
- tabs
- forms
- badges
- shadows
- borders
- radii

The visual treatment should come from the approved design system and creative concept.

## 7. Component boundaries

Create reusable components when one or more of these are true:

- the behavior is reused
- the content structure repeats meaningfully
- accessibility logic should be centralized
- a pattern must remain visually consistent
- the component has meaningful internal state or complexity

Do not create components only to make every file tiny.

Do not force unrelated sections into a generic Section component if doing so reduces creative control.

Aurex prefers reusable primitives plus composition-specific sections.

## 8. Content architecture

Content should be modeled separately from visual implementation where repetition or CMS use makes that valuable.

Avoid huge JSX files filled with duplicated content objects, inline SVGs, animation timelines, and page logic in one place.

Keep page-specific creative code close enough to the page that future developers can understand the experience without searching across an unnecessary abstraction layer.

## 9. Metadata and crawlability

For Next.js projects, use the Metadata API or supported file conventions for titles, descriptions, canonical behavior, robots, sitemaps, icons, and social images.

Important page content should exist in rendered HTML rather than depending on client-only fetching when there is no strong reason for it.

Do not create SEO-critical text only through canvas, WebGL, pseudo-elements, or inaccessible animation layers.

## 10. Fonts

Use `next/font` or an equivalent self-hosted/optimized strategy when using Next.js.

Prefer variable fonts when they provide the required visual range efficiently.

Limit font families and loaded weights to what the design actually uses.

Do not choose a font because it is fashionable. Typography should fit the brand and preserve readability.

## 11. Images and video

Use optimized responsive images and explicit dimensions or aspect ratios to prevent layout shift.

For Next.js, prefer `next/image` when appropriate.

Do not ship original multi-megabyte camera files directly to the browser.

Hero media requires special attention because it may become the Largest Contentful Paint element.

Video must have a reason to exist. Optimize dimensions, bitrate, codec, preload behavior, poster imagery, autoplay behavior, and mobile fallback intentionally.

Do not autoplay audio.

## 12. Animation architecture

Animation code should be organized around a motion system, not scattered one-off effects.

Prefer CSS for simple state transitions.

Prefer Motion for most React animation, layout transitions, reveals, gestures, and ordinary scroll-linked behavior.

Use GSAP/ScrollTrigger when the experience needs capabilities such as:

- coordinated timelines
- pinning
- scrubbed story sequences
- advanced parallax
- complex SVG choreography
- sophisticated scroll-state orchestration

Do not install multiple animation systems without a clear responsibility boundary.

## 13. Forms

Forms are production systems, not decorative UI.

A form implementation must account for:

- semantic labels
- keyboard behavior
- autocomplete attributes
- client feedback
- server validation
- spam protection
- failure states
- loading states
- duplicate submission behavior
- successful delivery
- analytics
- privacy implications
- CRM or notification routing

Never trust client-side validation alone.

## 14. Dependency discipline

Before adding a dependency, ask:

1. Does the platform already solve this?
2. Can a small amount of maintainable code solve it safely?
3. Is the dependency active, documented, and appropriate for the project?
4. What client-side JavaScript or CSS cost does it add?
5. Does it create vendor lock-in or maintenance risk?

Avoid dependency accumulation caused by convenience alone.

## 15. Environment and secrets

Secrets never belong in source control or browser bundles.

In Next.js, only values intentionally safe for the browser may use a public environment prefix.

Maintain `.env*` ignore rules appropriate to the framework.

Document required environment variable names without committing secret values.

## 16. Error handling

User-facing failures should be understandable and recoverable where possible.

Do not swallow exceptions silently.

For conversion flows, log enough context to diagnose delivery failures without logging sensitive information unnecessarily.

## 17. Production definition of done

A feature is not done because the code compiles.

Before a website is considered production-ready, Aurex must verify as relevant:

- production build succeeds
- type checking succeeds
- linting succeeds
- representative automated tests succeed
- key flows work in the browser
- forms deliver end to end
- metadata renders correctly
- crawl controls are correct
- accessibility checks pass to the project standard
- mobile is intentionally reviewed
- motion respects reduced motion
- no material console errors remain
- no secrets are exposed
- analytics events fire correctly
- images, fonts, and video are optimized
- performance is within the Aurex standard

## 18. Final principle

Engineering should make the creative concept feel inevitable, not fragile.

If an implementation only works at one viewport, depends on excessive JavaScript, breaks accessibility, harms SEO, or requires constant hacks to preserve the visual concept, the engineering solution is not finished.