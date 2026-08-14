---
paths:
  - "app/**/*.{ts,tsx,js,jsx}"
  - "pages/**/*.{ts,tsx,js,jsx}"
  - "src/**/*.{ts,tsx,js,jsx}"
---

# SEO Rendering Rules

- Important page content must be present in rendered HTML unless there is a strong product reason for client-only delivery.
- Use the framework's supported metadata APIs and file conventions for titles, descriptions, canonical behavior, robots, sitemaps, favicons, and social metadata.
- Every indexable page needs a distinct purpose. Do not create thin pages only to target a keyword variation.
- Do not hide important text in canvas, WebGL, images, CSS pseudo-elements, or animation-only layers.
- Heading structure must follow content hierarchy, not visual font size.
- Internal links should connect genuinely related service, location, proof, and educational pages.
- Link text should communicate destination meaning when possible.
- Structured data must match visible content and supported schema use cases. Do not manufacture ratings, reviews, locations, services, FAQs, prices, or business facts.
- Preserve valuable existing URLs during rebuilds or create intentional redirects.
- Avoid accidental `noindex`, canonical mistakes, staging-domain canonicals, duplicate metadata, and robots rules that block required assets or pages.
- For local businesses, keep name, address, phone, service area, location relationships, and business facts accurate and internally consistent.
- Do not sacrifice readable copy for exact-match keyword repetition.
- Research current search-engine guidance before making a material SEO decision that may have changed.