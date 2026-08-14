---
name: aurex-technical-qa
description: Runs the production-readiness technical audit for an Aurex site across build, typing, linting, browser console, metadata, crawlability, accessibility, responsive behavior, security, integrations, and representative automated tests. Use before final creative review and launch.
---

# Aurex Technical QA

This skill verifies the system beneath the design.

Do not substitute this for visual QA. Run both.

## 1. Build and static checks

Run the project's real configured commands for:

- production build
- type checking
- linting
- automated tests

Do not invent command names. Read `package.json` and project documentation first.

## 2. Browser smoke test

Inspect representative pages and page patterns.

Verify:

- page renders
- no material console errors
- navigation works
- primary CTAs work
- images/media load
- interactive controls work
- direct route loads work
- 404/not-found behavior works

## 3. Responsive smoke test

Test representative desktop, tablet, and mobile widths.

Check overflow, clipping, fixed/sticky elements, navigation, forms, media crops, and complex animation.

## 4. SEO/crawlability

Verify representative pages for:

- title
- description
- canonical
- indexability
- heading structure
- rendered content
- sitemap presence
- robots behavior
- redirects where required
- structured data syntax and factual accuracy where used

## 5. Accessibility

Run configured automated accessibility checks.

Manually test:

- keyboard navigation
- focus visibility
- primary form
- navigation/menu
- dialogs or custom controls
- reduced motion

## 6. Security baseline

Check:

- no exposed secrets
- public environment variables are intentionally public
- server inputs are validated
- public forms have appropriate abuse controls
- user-facing errors do not leak internal detail
- webhook verification exists when required

## 7. Integrations

Test configured:

- forms/CRM
- analytics
- advertising conversions
- scheduling
- call tracking
- maps/location tools
- CMS content
- other business-critical integrations

## 8. Report severity

Classify issues:

### Blocker
Cannot safely/reliably launch.

### Critical
Likely business, accessibility, SEO, or security impact.

### Important
Material quality issue that should be addressed.

### Polish
Low-risk cleanup.

## Output

### Verdict
Ready / Ready after listed fixes / Not ready

### Blockers
Put these first.

### Verification matrix
What was tested and result.

### Unverified items
Anything unavailable because credentials, production services, content, or access were missing.

### Recommended next step
Exact remaining work before launch.