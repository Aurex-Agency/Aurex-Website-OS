---
name: aurex-launch
description: Coordinates final Aurex website launch readiness, production configuration, redirects, forms, tracking, SEO controls, domain/DNS, deployment, smoke testing, and post-launch verification. Use only after creative and technical QA are substantially complete.
disable-model-invocation: true
---

# Aurex Launch

A launch is a controlled transition, not merely a deploy button.

## Preconditions

Do not launch while known blockers remain in:

- primary conversion
- accessibility
- crawlability/indexability
- security
- production build
- domain/DNS
- critical integrations

## 1. Confirm approved scope

Verify:

- approved pages exist
- content is final enough to launch
- required legal/client-provided policies are present
- placeholders are explicitly approved or removed
- no staging copy or test data remains

## 2. Production configuration

Verify:

- correct production environment variables
- secure secrets store
- production API/integration endpoints
- analytics production IDs
- error/reporting configuration where used
- correct site URL/base URL

## 3. SEO migration

For rebuilds, create and verify redirects from valuable old URLs to the most relevant new destination.

Check:

- production canonicals
- robots
- sitemap
- metadata
- no staging noindex rules carried into production
- no production URLs accidentally pointing to preview/staging domains

## 4. Conversion systems

Submit production-safe test leads.

Verify:

- delivery
- CRM
- notifications
- booking
- call tracking where applicable
- analytics
- advertising conversion events

## 5. Domain and DNS

Before changing DNS, record:

- current provider
- current relevant records
- target records
- rollback information
- email-related records that must not be disturbed

Do not casually replace all DNS records when only web records need change.

## 6. Deploy

Deploy using the project's documented production method.

Record the production version/commit.

## 7. Immediate smoke test

On the real production domain test:

- homepage
- navigation
- representative internal pages
- primary lead flow
- mobile
- HTTPS
- redirects
- 404
- metadata
- robots/sitemap
- analytics
- console errors

## 8. Post-launch search checks

Where access exists:

- verify sitemap submission/discovery
- inspect representative production URLs
- confirm important pages are crawlable
- monitor redirect/404 issues

Do not promise immediate ranking changes.

## 9. Post-launch performance

Run a production performance smoke test after CDN/cache behavior settles enough for a meaningful check.

Establish field monitoring when available.

## 10. Rollback

For material launches, know how to restore the prior deployment or configuration if a critical issue appears.

## Output

### Launch verdict
Approved / Blocked

### Production version
Commit/deployment reference.

### Conversion verification
Results of real production-safe tests.

### SEO verification
Robots, sitemap, canonical, redirects, indexability.

### Domain verification
Production hostname and HTTPS status.

### Remaining observations
Non-blocking post-launch work.

### Monitoring plan
What should be checked over the following days/weeks as real data becomes available.