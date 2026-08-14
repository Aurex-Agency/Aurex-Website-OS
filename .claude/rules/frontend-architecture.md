---
paths:
  - "**/*.{ts,tsx,js,jsx}"
---

# Frontend Architecture Rules

- For new Aurex marketing sites, default to Next.js App Router + TypeScript unless project requirements justify another stack.
- Preserve an existing project stack unless migration provides a material business or technical benefit.
- Prefer React Server Components for content-heavy UI. Add `use client` only at the lowest practical boundary that needs browser behavior.
- Do not convert a whole page or layout to a client component to support one animated or interactive child.
- Keep SEO-critical and primary page content available in rendered HTML.
- Use framework metadata APIs and file conventions instead of manually duplicating head-tag logic across pages.
- Model repeated business content with typed structures when it improves maintainability, but do not over-abstract unique creative sections.
- Prefer reusable primitives plus page-specific composition. Do not force unrelated sections through one generic Section/Card system.
- Validate untrusted runtime data at server/API boundaries.
- Avoid `any` unless the reason is genuinely unavoidable and documented.
- Before installing a package, check whether the framework, browser, existing dependency, or a small maintainable utility already solves the problem.
- Keep secrets server-side. Never expose a private credential because a client component needs it.
- Production behavior must be verified with a production build, not inferred from development mode.