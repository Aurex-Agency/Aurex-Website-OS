---
paths:
  - "**/*.{ts,tsx,js,jsx}"
---

# Forms and Analytics Rules

- Treat lead forms as production-critical systems.
- Collect the minimum information needed for the current conversion step.
- Client-side validation is UX only. Validate submitted data again on the server or trusted backend.
- Every required field must have a business reason.
- Multi-step forms must reduce genuine complexity, not disguise an unnecessarily long questionnaire.
- Define loading, success, validation, network failure, provider failure, and duplicate-submit states.
- Do not clear user input on a recoverable failure unless there is a strong reason.
- Test the real destination: CRM, email, webhook, booking system, database, or other endpoint. A success toast without confirmed delivery is not sufficient QA.
- Public endpoints need reasonable spam/abuse protection appropriate to risk.
- Conversion event names must represent business meaning, not DOM implementation.
- Do not send names, emails, phone numbers, free-form messages, health details, financial details, or other sensitive personal data into analytics events.
- Prevent duplicate conversion events caused by rerenders, route transitions, retries, or thank-you page reloads.
- Distinguish form start, form submit, lead, qualified lead, appointment, and sale. Do not inflate reporting by renaming an upstream interaction as a downstream business result.
- Verify analytics and advertising events in debug tools before launch.
- If consent or legal requirements are uncertain, escalate rather than inventing a compliance rule.