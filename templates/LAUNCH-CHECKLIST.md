# Aurex Launch Checklist

## Launch status

**Client:**

**Production domain:**

**Production commit/deployment:**

**Launch owner:**

**Status:** Blocked / Ready with conditions / Ready / Launched

## 1. Approval

- [ ] Desktop homepage visually approved
- [ ] Dedicated mobile art-direction pass complete
- [ ] Human mobile visual approval recorded with date and reviewed commit/deployment
- [ ] ChatGPT mobile visual approval recorded with review reference, date, and reviewed commit/deployment
- [ ] All required page bundles approved
- [ ] Final creative review complete
- [ ] Technical QA complete
- [ ] Accessibility review complete
- [ ] Conversion/form QA complete
- [ ] Remaining placeholders explicitly approved or removed

## 2. Production build

- [ ] Typecheck passes
- [ ] Lint passes
- [ ] Configured tests pass
- [ ] Production build passes
- [ ] Representative production-like browser test passes
- [ ] No material browser console errors remain

## 3. Production configuration

- [ ] Production environment variables configured
- [ ] No secret values committed
- [ ] Public environment variables intentionally public
- [ ] Production service endpoints configured
- [ ] Correct production site/base URL configured
- [ ] Preview/staging-only values removed

## 4. Domain and DNS

- [ ] Current DNS records documented before change
- [ ] Required target records confirmed
- [ ] Email/MX/SPF/DKIM/DMARC records preserved unless intentionally changed
- [ ] Verification records preserved unless intentionally changed
- [ ] Production hostname resolves correctly
- [ ] HTTPS valid
- [ ] Preferred hostname redirect works

## 5. SEO and migration

- [ ] Production titles/descriptions verified
- [ ] Canonicals point to production URLs
- [ ] Robots behavior correct
- [ ] XML sitemap available and correct
- [ ] No accidental site-wide noindex
- [ ] Important pages render crawlable content
- [ ] Structured data validated where used
- [ ] Old-to-new redirect map implemented for rebuilds
- [ ] Important legacy URLs tested
- [ ] 404 behavior verified
- [ ] Internal links do not point to staging/preview URLs

## 6. Primary conversion

For every business-critical conversion:

- [ ] Real production-safe test completed
- [ ] Success state works
- [ ] Failure state works
- [ ] Backend/CRM receives correct data
- [ ] Internal notification works
- [ ] Booking/scheduling works where relevant
- [ ] Call/text links work on mobile
- [ ] Duplicate behavior acceptable
- [ ] Spam protection active where required

## 7. Analytics and advertising

- [ ] GA4/analytics installed with production configuration
- [ ] Primary conversion event fires only on success
- [ ] Secondary events verified
- [ ] Google Ads conversion tracking verified where used
- [ ] Meta tracking verified where used
- [ ] Call tracking verified where used
- [ ] No sensitive form values/PII are sent in analytics events
- [ ] Consent behavior matches approved implementation

## 8. Accessibility

- [ ] Automated accessibility scan run where configured
- [ ] Keyboard navigation manually reviewed
- [ ] Focus visible
- [ ] Sticky/floating UI does not obscure focused controls
- [ ] Primary form manually completed by keyboard
- [ ] Navigation/menu manually tested
- [ ] Dialog/custom controls tested where used
- [ ] Reduced-motion experience verified
- [ ] Important contrast issues resolved

## 9. Responsive

Technically responsive is not creatively approved. Do not mark launch ready unless the separate mobile approval gate above is complete.

- [ ] Large desktop reviewed
- [ ] Laptop/small desktop reviewed
- [ ] Tablet reviewed
- [ ] 390x844 reviewed through meaningful scroll states
- [ ] 393x852 reviewed through meaningful scroll states
- [ ] Representative width around 430px reviewed through meaningful scroll states
- [ ] Intermediate responsive transitions reviewed
- [ ] Navigation works at all representative sizes
- [ ] Forms work with mobile keyboard
- [ ] No material horizontal overflow
- [ ] Media crops remain intentional
- [ ] Mobile image focal points/crops were decided per viewport rather than inherited by default
- [ ] Sticky UI does not block content or conversion
- [ ] Signature motion has a valid mobile behavior
- [ ] Sticky/scroll-linked sections complete their full mobile sequence and preserve native scrolling
- [ ] Touch interactions and non-hover alternatives work
- [ ] Mobile content density and pacing are intentionally composed
- [ ] Primary CTAs remain visible, reachable, and comfortable to use

## 10. Performance

- [ ] Production-like performance audit run
- [ ] LCP element understood
- [ ] Hero media optimized
- [ ] Font loading reviewed
- [ ] Third-party scripts reviewed
- [ ] Layout shift issues addressed
- [ ] Heavy motion reviewed on mobile
- [ ] No unexplained major performance regression remains
- [ ] Post-launch field monitoring plan defined where practical

## 11. Content and trust

- [ ] No test/lorem placeholder copy remains
- [ ] Contact information accurate
- [ ] Service/location information accurate
- [ ] Claims have appropriate support
- [ ] Review/testimonial attribution accurate
- [ ] Copyright/year/company details correct
- [ ] Social links correct
- [ ] Favicon/site identity correct
- [ ] OG/social sharing appearance reviewed

## 12. Security and privacy

- [ ] Public inputs validated server-side
- [ ] Public forms have appropriate abuse controls
- [ ] Webhook signatures verified where supported
- [ ] User-facing errors do not expose sensitive detail
- [ ] No known exposed credentials
- [ ] High-risk dependency issues reviewed
- [ ] Privacy-sensitive integrations documented

## 13. Rollback

- [ ] Previous production state known where applicable
- [ ] Deployment rollback method known
- [ ] DNS rollback information recorded when DNS changes are involved
- [ ] Responsible person knows what qualifies as a rollback-triggering issue

## 14. Immediate post-launch smoke test

On the real production domain:

- [ ] Homepage
- [ ] Navigation
- [ ] Representative service/product page
- [ ] Representative trust/content page
- [ ] Primary conversion
- [ ] Mobile conversion
- [ ] Redirects
- [ ] 404
- [ ] Analytics
- [ ] Console
- [ ] Robots/sitemap
- [ ] Canonical

## 15. Post-launch follow-up

- [ ] Search console/sitemap follow-up scheduled where applicable
- [ ] 404/redirect monitoring planned
- [ ] Real conversion delivery monitored
- [ ] Field Core Web Vitals reviewed when enough data exists
- [ ] Early client feedback captured
- [ ] Repeatable lessons proposed back to Aurex Website OS

## Blockers

List anything that prevents launch.

## Conditions

List accepted non-blocking items and owner/date.

## Final approval

**Approved by:**

**Date/time:**

**Production deployment:**
