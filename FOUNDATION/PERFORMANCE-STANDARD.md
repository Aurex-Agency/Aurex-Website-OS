# Aurex Performance Standard

Performance is part of perceived quality, conversion, accessibility, and organic visibility. Aurex does not treat it as a final optimization sprint.

## Core Web Vitals targets

Use field data as the primary long-term signal when available.

Target the current Core Web Vitals good thresholds at the 75th percentile on both mobile and desktop:

- LCP: 2.5 seconds or less
- INP: 200 milliseconds or less
- CLS: 0.1 or less

Lab scores are diagnostic tools, not business outcomes. Do not claim a site is fast only because Lighthouse returns a high score.

## 1. Performance budgets are architectural

Before adding expensive media, libraries, scripts, or animation, understand the cost.

Ask:

- Is this above the fold?
- Could this become LCP?
- Does it require client JavaScript?
- Does it block rendering?
- Does it add third-party network work?
- Does it shift layout after load?
- Does it run continuously?
- Does the same effect exist on mobile?
- Is the perceived-value gain worth the cost?

## 2. Largest Contentful Paint

Protect likely LCP elements.

For hero imagery:

- size and compress intentionally
- serve responsive dimensions
- use modern formats when supported by the stack
- avoid loading a desktop-sized asset on mobile
- do not lazy-load the true LCP image
- provide stable dimensions
- avoid delaying visibility behind unnecessary entrance animation

For hero video:

- determine whether video is worth the loading cost
- provide a strong poster frame
- avoid making video completion necessary to understand the message
- consider a static mobile fallback when bandwidth or viewport makes video wasteful
- avoid huge source files and unnecessary resolution

## 3. JavaScript discipline

Ship less browser JavaScript by default.

Prefer server components and platform capabilities for content-heavy areas.

Keep client components small and interaction-specific.

Dynamically load heavy optional experiences where appropriate.

Do not make static content dependent on hydration without a clear reason.

Audit large libraries, duplicated utilities, animation packages, maps, chat widgets, review widgets, and tracking scripts.

## 4. Third-party scripts

Every third-party script must have an owner and reason.

Examples include:

- analytics
- advertising pixels
- chat
- call tracking
- review widgets
- maps
- scheduling
- CRM embeds

Load scripts with appropriate framework primitives and timing. Avoid blocking the critical path when the script is not required for first paint or immediate interaction.

Remove abandoned tools instead of letting tags accumulate forever.

## 5. Fonts

Use optimized/self-hosted font delivery where practical.

Load only the families, styles, subsets, and weights actually used.

Use variable fonts when they reduce requests and still fit the design.

Prevent font loading from causing avoidable layout shift.

## 6. Images

Treat image dimensions as content decisions.

Use:

- responsive `srcset`/framework image optimization
- correct `sizes`
- explicit dimensions or aspect ratios
- appropriate quality
- modern formats
- lazy loading below the fold
- priority only for genuinely critical imagery

Do not globally set every image to maximum quality.

Do not use CSS background images for important semantic imagery when an actual image element provides better responsive loading, accessibility, and optimization.

## 7. Video

Video should be compressed for its placement, not exported at master-delivery quality.

Avoid multiple autoplaying videos in the same viewport.

Pause or avoid expensive off-screen playback where practical.

Respect `prefers-reduced-motion` where motion is non-essential.

## 8. Animation performance

Prefer transform and opacity animation for high-frequency motion.

Avoid layout-thrashing animation patterns.

Do not leave `will-change` applied globally or indefinitely without reason.

For scroll animation:

- avoid attaching expensive work directly to unthrottled scroll handlers
- use animation libraries or browser primitives that batch efficiently
- clean up observers, listeners, timelines, and ScrollTriggers
- test resize behavior
- test lower-powered mobile devices

## 9. Layout stability

Reserve space for:

- images
- embeds
- video
- ads when applicable
- dynamic notices
- third-party widgets

Avoid injecting banners or late-loading content above existing content without accounting for layout movement.

## 10. Route strategy

Do not render every page dynamically when content can be cached or pre-rendered.

Do not statically freeze content that requires real-time accuracy.

Choose rendering and caching intentionally based on content freshness, personalization, operational complexity, and SEO.

## 11. Measurement workflow

During development:

- inspect network and bundle behavior
- test representative mobile viewport/device conditions
- run production builds
- test production-like output, not only dev mode

Before launch:

- run Lighthouse or equivalent lab diagnostics on representative pages
- inspect LCP element and request waterfall
- check CLS sources
- test key interactions for responsiveness
- inspect route JavaScript where it appears excessive

After launch:

- prefer real-user or CrUX field data when enough traffic exists
- investigate regressions by template/page group
- compare mobile and desktop separately

## 12. Aurex internal release expectation

Performance issues are launch blockers when they materially harm usability, conversion, crawlability, or accessibility.

A weak Lighthouse score alone is not automatically a blocker, but every significant warning should be understood rather than dismissed.

A creative effect that causes unacceptable performance should be redesigned, not defended because it looks impressive on a development laptop.