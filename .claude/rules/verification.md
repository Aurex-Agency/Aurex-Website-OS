# Verification Rules

- Do not declare a website, page, form, or major interaction finished from code inspection alone.
- Run the project's real production build before launch readiness.
- Run type checking and linting when configured.
- Use the browser to inspect representative pages at desktop and mobile sizes.
- For visually significant work, review mobile at 390x844, 393x852, and a representative width around 430px. Inspect meaningful scroll states and resize through intermediate widths.
- Reproduce and test the primary conversion path end to end.
- Check browser console output for material errors and warnings.
- Verify metadata, canonical behavior, robots/indexability, and sitemap output on representative pages.
- Verify images, video, fonts, and third-party scripts in the network panel when performance matters.
- Run automated accessibility checks when configured, then manually test keyboard navigation and complex interactions.
- Verify reduced-motion behavior on pages with meaningful animation.
- Verify viewport-specific image crops/focal points, touch interactions, content density, CTA usability, and the complete entry-to-exit behavior of sticky or scroll-linked sections.
- A responsive technical pass does not constitute mobile creative approval. Record separate desktop and mobile verdicts, and do not enter launch readiness without explicit human + ChatGPT mobile approval.
- Test real responsive transitions, not only two screenshots.
- For multi-page sites, test one representative page from every shared page pattern plus strategically unique pages.
- When a fix changes layout, animation, media, or interactivity, visually inspect the affected result again.
- Distinguish blockers from polish. Never hide a blocker inside a long list of minor findings.
- If a required verification cannot be performed, state exactly what remains unverified and why.
