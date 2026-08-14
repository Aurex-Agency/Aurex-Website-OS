---
paths:
  - "**/*.{ts,tsx,js,jsx,css,scss}"
---

# Media and Font Rules

- On Next.js projects, prefer `next/image` for responsive raster imagery when appropriate and `next/font` for optimized font delivery.
- Always provide stable image dimensions or aspect ratios to avoid layout shift.
- Set image `sizes` intentionally. Do not make every responsive image effectively request desktop width.
- Do not lazy-load the actual LCP image.
- Do not mark many images as priority. Priority is for truly critical above-the-fold media.
- Compress source imagery for web delivery. Never ship original camera exports directly because they happen to look sharp.
- Decorative imagery should have empty alt text when semantically appropriate. Informative imagery needs purpose-based alt text.
- Hero video must include a deliberate poster and fallback strategy. It cannot be required to understand the core offer.
- Avoid autoplay audio.
- Consider static or lighter mobile alternatives for heavy video or advanced media.
- Do not use important semantic imagery only as a CSS background if doing so weakens responsive loading, accessibility, or SEO.
- Load only font families, weights, styles, and subsets used by the design.
- Prefer variable fonts when they provide needed range efficiently.
- Do not pick a typeface because it is trendy or because another Aurex project used it. Typography belongs to the current brand.