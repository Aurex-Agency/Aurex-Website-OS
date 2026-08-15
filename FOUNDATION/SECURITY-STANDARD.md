# Aurex Security Standard

Aurex websites are often marketing sites, but forms, analytics, CMSs, integrations, account portals, payment links, and server actions still create real security and privacy responsibilities.

This standard is a baseline, not a substitute for specialized security review on high-risk systems.

## 1. Secrets

Never commit secrets, tokens, API keys, private credentials, passwords, or production connection strings.

Only values explicitly intended for browser exposure may be included in public environment variables.

Document required variable names in an example environment file using fake values.

Keep local and production secret stores separate from source control.

## 2. Server boundaries

Treat every request from the browser as untrusted.

Server Actions, Route Handlers, APIs, webhooks, and form endpoints must validate input and enforce the permissions or assumptions they depend on.

Do not assume that hiding a button prevents a user from calling the underlying endpoint.

## 3. Input validation

Validate user-controlled data at the server boundary.

Check:

- required fields
- types
- expected lengths
- allowed values
- file type/size when uploads exist
- URLs and identifiers
- business rules

Reject malformed or unexpected input safely.

Client-side validation improves UX but is not a security boundary.

## 4. Output safety

Do not inject untrusted HTML into the DOM.

Avoid `dangerouslySetInnerHTML` for user or third-party content unless the content is properly sanitized and the risk is understood.

Escape or sanitize content at the appropriate boundary.

## 5. Public lead forms

Public forms should account for abuse.

Depending on risk and volume, use a combination of:

- server validation
- honeypot fields
- rate limiting
- timing/behavior checks
- CAPTCHA or managed challenge only when justified
- duplicate detection
- provider-level spam controls

Do not create an unnecessarily hostile form experience for legitimate users simply to fight spam.

## 6. Webhooks

Verify webhook signatures when the provider supports them.

Do not trust a webhook because the payload shape looks correct.

Make handlers idempotent when duplicate delivery is possible.

Avoid logging full sensitive payloads without need.

## 7. Authentication and authorization

If a project includes authenticated areas, authorization must be checked server-side for protected data and actions.

Authentication proves identity. Authorization determines what that identity may do. Do not confuse the two.

Do not build custom authentication when a well-supported solution fits the project unless there is a strong reason.

## 8. External links and embeds

Review third-party embeds for:

- privacy impact
- script permissions
- performance impact
- trustworthiness
- data collection

Use secure external URLs.

For links opening new tabs, use browser-safe patterns appropriate to the framework.

## 9. Content Security Policy

Consider a Content Security Policy on production sites, especially when third-party scripts, embedded content, or user-generated content increase exposure.

Do not ship a copied CSP that breaks required functionality or uses broad unsafe directives without understanding why.

Build policy from the scripts and origins the site actually needs.

## 10. Dependencies

Keep dependencies reasonably current and remove unused packages.

Review security advisories for material vulnerabilities.

Do not blindly apply breaking automated upgrades to production sites without understanding the impact.

## 11. Error handling

User-facing errors should not expose:

- stack traces
- secret values
- internal file paths
- database details
- provider credentials
- sensitive user data

Log diagnostic information appropriately on the server.

## 12. Privacy and data minimization

Collect only the information the business reasonably needs.

Do not store sensitive information in analytics events, URLs, browser storage, or logs without a justified need and appropriate safeguards.

Consider applicable consent and privacy requirements for analytics, advertising, call tracking, cookies, and form data.

Do not invent legal compliance claims. Escalate legal-policy decisions to the client or qualified counsel when necessary.

## 13. File uploads

If file upload is required:

- restrict accepted types
- restrict size
- do not trust file extensions alone
- isolate storage appropriately
- avoid executing uploaded content
- use provider security features
- consider malware scanning when risk warrants it

## 14. Production review

Before launch, check:

- no secrets in repository or client bundle
- environment variables are correctly scoped
- public endpoints validate input
- forms have reasonable abuse protection
- webhook verification exists where appropriate
- authenticated actions enforce authorization
- dependencies have no ignored critical issues without rationale
- error states do not leak sensitive detail
- analytics avoid sensitive payloads
- production-only integrations are configured through secure secret stores

## 15. Security versus convenience

A feature that only works by exposing a secret, trusting browser input, or disabling a security control is not production-ready.

Find a proper architecture instead of documenting the vulnerability as a workaround.