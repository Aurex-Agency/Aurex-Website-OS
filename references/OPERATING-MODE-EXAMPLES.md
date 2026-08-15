# Aurex Operating Mode Examples

Use these examples to calibrate QUICK, STANDARD, and DEEP decisions. They are examples, not rigid rules.

## QUICK examples

### Change a homepage CTA label

Task: Change `Request a Quote` to `Get My Free Estimate` on the approved homepage.

Mode: QUICK

Why: Bounded copy/UI change inside an approved conversion system.

Likely context:

- current component
- relevant copy/design-system rule

Likely verification:

- route renders
- CTA destination still correct
- mobile layout unaffected

Specialist: none

### Replace an image

Task: Replace a weak service photo with a new client-provided image and adjust crop.

Mode: QUICK

Why: No strategy or page architecture change.

Specialist: none

### Fix one mobile overflow bug

Mode: QUICK

Why: Known technical defect with clear acceptance criteria.

Verification: affected widths plus targeted lint/typecheck where relevant.

### Add another service page using an approved page-category pattern

Mode: QUICK or STANDARD depending on content novelty.

QUICK when structure, conversion role, SEO intent, and design pattern are already approved and the new page is a straightforward application.

STANDARD when the new service has different customer intent, proof needs, form flow, or content architecture.

## STANDARD examples

### Redesign the homepage services section

Task: Current equal-card grid feels generic and weakens the approved creative direction.

Mode: STANDARD

Why: Meaningful visual and conversion change, but the overall website strategy is already approved.

Likely context:

- `CREATIVE-DIRECTION.md`
- `DESIGN-SYSTEM.md`
- homepage section implementation
- relevant conversion strategy

Likely skills:

- `/aurex-page-design`
- `/aurex-engineering`
- `/aurex-visual-qa`

Possible specialist: Creative Director if multiple strong compositions remain.

### Build a new multi-step estimate flow

Mode: STANDARD

Why: Material conversion and technical work, but not necessarily a full-site strategy change.

Likely skills:

- `/aurex-conversion`
- `/aurex-engineering`
- `/aurex-form-qa`

Possible specialist: Conversion Strategist for field/step logic.

### Implement an already approved homepage concept

Mode: STANDARD

Why: The expensive creative decision has already been made. Implementation needs significant engineering, responsive, motion, and browser work, but should not redo discovery or art direction.

Possible specialists: Frontend Architect or Motion Director only where specific complexity warrants it.

### Add a new service-page category pattern

Mode: STANDARD

Why: The pattern will be reused, so visual hierarchy, conversion, SEO intent, and component architecture deserve deliberate work.

After the pattern is approved, subsequent pages may drop to QUICK.

### Targeted SEO audit of service pages

Mode: STANDARD

Why: Focused discipline-specific audit. It does not justify redoing creative discovery or the entire website strategy.

## DEEP examples

### New client website

Mode: DEEP

Why: Strategy, architecture, conversion, content, creative direction, and engineering decisions are not yet settled.

Use specialists deliberately across stages, not all at once.

### Major redesign with new positioning

Mode: DEEP

Why: Existing decisions may no longer be valid. Requires strategic and creative re-evaluation before implementation.

### Site migration with high organic traffic

Mode: DEEP

Why: Redirects, indexability, canonicals, rendering, content preservation, analytics, and launch safety create material risk.

Likely specialists:

- SEO Strategist
- Frontend Architect
- Launch Engineer

### Final pre-launch gate for a significant client site

Mode: DEEP

Why: Multiple business-critical systems need comprehensive verification before production cutover.

Deep review does not mean redoing discovery. It means broad verification against approved strategy.

## Common mode mistakes

### Mistake: client is important, therefore DEEP

Wrong.

A Fortune 500 client's typo fix is still QUICK.

Mode follows the work unit, not the prestige of the client.

### Mistake: new page, therefore DEEP

Wrong.

A new page using an approved reusable pattern may be QUICK.

### Mistake: animation, therefore Motion Director

Wrong.

Simple motion inside an established motion system usually stays in the primary session.

### Mistake: SEO mentioned, therefore full SEO audit

Wrong.

Use the minimum SEO context required for the current decision.

### Mistake: full site is in the repo, therefore read the full site

Wrong.

Start from project artifacts and relevant files. Expand only when the task requires it.

## Escalation examples

### QUICK -> STANDARD

A requested button-label change reveals that different CTAs route to inconsistent forms and analytics events.

Reason: the problem is now conversion-system-wide rather than a bounded copy edit.

### STANDARD -> DEEP

While creating a new service-page architecture, research shows the current URL structure conflicts with a planned domain migration and several existing high-value organic pages.

Reason: the decision now has migration and organic-risk implications.

### STANDARD stays STANDARD

A homepage redesign reveals several small responsive defects in adjacent sections.

Do not escalate to DEEP merely because scope expanded slightly. Keep the task bounded and create follow-up work if necessary.
