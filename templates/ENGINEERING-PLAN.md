# Aurex Engineering Plan

## Project

**Client:**

**Repository:**

**Approved creative direction:**

**Primary conversion:**

## 1. Stack

**Framework/version:**

**Language:**

**Styling:**

**Package manager:**

**Deployment:**

**CMS/data source:**

**Primary animation system:**

**Advanced animation system, if needed:**

### Non-default choices

Document any stack decision that differs from Aurex defaults and why.

## 2. Rendering and routing

**Rendering strategy:**

**Pages/routes:**

**Dynamic routes:**

**Caching/revalidation needs:**

**SEO-critical content rendering considerations:**

## 3. Server/client boundaries

List major client components and why browser execution is required.

| Component/area | Why client-side | Cost/risk | Alternative considered |
|---|---|---|---|

## 4. Design-system implementation

**Token strategy:**

**Typography loading:**

**Color/surface tokens:**

**Spacing/container strategy:**

**Shared primitives:**

**Component-library primitives used:**

Document how library defaults will be visually replaced by the client design system.

## 5. Media plan

| Asset | Page/section | Delivery strategy | LCP risk | Mobile strategy | Status |
|---|---|---|---|---|---|

## 6. Motion architecture

**Motion intensity:**

**CSS responsibilities:**

**Motion responsibilities:**

**GSAP/ScrollTrigger responsibilities:**

**Reduced-motion behavior:**

**Performance-sensitive sequences:**

## 7. Forms and conversions

| Conversion | Frontend | Server/destination | Validation | Spam control | Tracking |
|---|---|---|---|---|---|

**Failure/retry behavior:**

**Post-submit behavior:**

## 8. Analytics and integrations

| Integration | Purpose | Client/server | Required env vars | Verification method |
|---|---|---|---|---|

Do not include secret values.

## 9. SEO implementation

**Metadata pattern:**

**Sitemap:**

**Robots:**

**Canonical strategy:**

**Structured data:**

**Redirect requirements:**

## 10. Accessibility plan

**Target:** WCAG 2.2 AA unless otherwise documented

**High-risk interactions:**

**Automated testing:**

**Manual testing:**

## 11. Performance plan

**Likely LCP elements:**

**Heavy dependencies:**

**Third-party scripts:**

**Video/animation risks:**

**Field monitoring plan:**

## 12. Quality automation

**Typecheck command:**

**Lint command:**

**Test command:**

**Build command:**

**E2E command:**

**Accessibility command:**

**Claude hooks installed:**

**CI workflow:**

## 13. Security baseline

**Server validation:**

**Public endpoint protection:**

**Webhook verification:**

**Secret storage:**

**Privacy-sensitive integrations:**

## 14. Architectural risks

Rank by impact.

| Risk | Impact | Likelihood | Mitigation | Owner |
|---|---|---|---|---|

## 15. Decisions requiring human approval

Only list expensive-to-reverse, strategically material, or ownership/cost decisions.

## 16. Engineering status

**Status:** Draft / Approved / Implementing / QA / Production ready

**Last updated:**
