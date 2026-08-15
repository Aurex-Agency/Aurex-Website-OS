---
paths:
  - "**/*.{ts,tsx,js,jsx,json,yml,yaml}"
---

# Security Implementation Rules

- Never commit secrets or copy production credentials into source files, examples, tests, logs, or browser code.
- Treat all browser input as untrusted.
- Validate form, API, Server Action, webhook, CMS, query-string, and third-party data at the server boundary when correctness or security depends on it.
- Hidden UI is not authorization. Protected actions and data require server-side authorization.
- Do not render unsanitized untrusted HTML.
- Verify webhook signatures when supported by the provider.
- Make webhook/lead handlers idempotent when duplicate delivery is possible.
- Avoid logging full sensitive form payloads.
- Public form endpoints need reasonable abuse controls.
- Do not put sensitive values in URLs, analytics events, browser storage, or public environment variables.
- Review third-party scripts and embeds for privacy, permissions, and data collection as well as performance.
- Keep dependencies reasonably current and investigate material security advisories.
- User-facing errors must not expose stack traces, internal paths, secret values, database details, or provider credentials.
- Do not make legal or regulatory compliance claims without authoritative requirements for the specific client and jurisdiction.