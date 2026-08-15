---
name: aurex-form-qa
description: Tests an Aurex lead, booking, quote, application, or contact flow end to end, including UX, validation, accessibility, delivery, analytics, failure states, spam controls, and mobile behavior. Use before approving any primary conversion flow.
---

# Aurex Form QA

A form is not verified because clicking Submit shows a success message.

Use `FOUNDATION/LEAD-CONVERSION-STANDARD.md`, `FOUNDATION/ANALYTICS-STANDARD.md`, and the forms/analytics rules.

## Step 1: Define expected behavior

Document:

- conversion purpose
- required fields
- optional fields
- validation rules
- destination
- notifications
- analytics events
- success behavior
- failure behavior
- expected response promise

## Step 2: UX review

Check:

- first step is appropriately low-friction
- every field is justified
- labels are clear
- CTA communicates the action
- reassurance is present when useful
- progress is understandable for multi-step forms
- mobile keyboard/input behavior is appropriate
- user input survives recoverable errors when practical

## Step 3: Validation testing

Test:

- empty submit
- invalid email/phone/format where relevant
- boundary lengths
- required selections
- unexpected values
- server-side rejection

Confirm client and server feedback remain understandable.

## Step 4: Accessibility

Test:

- labels
- keyboard completion
- focus on errors
- error association
- status/success announcement where appropriate
- visible focus
- mobile/touch targets

## Step 5: Delivery

Submit real safe test data through the actual configured path.

Verify:

- backend receives submission
- CRM/contact record is correct
- email/SMS/internal notification fires where required
- duplicate behavior is acceptable
- provider failure is handled

## Step 6: Analytics

Verify:

- form_start only fires when appropriate
- step events are not duplicated
- form_submit fires only after the intended success condition
- advertising conversions fire at the correct point
- no PII or sensitive form values are leaked into analytics payloads

## Step 7: Abuse behavior

Review:

- rapid duplicate submits
- honeypot/challenge/rate limit when configured
- obvious bot behavior
- retry path for legitimate users

## Step 8: Mobile

Complete the entire flow at a representative mobile width.

Check keyboard overlap, sticky controls, viewport jumps, error scrolling, progress, and final confirmation.

## Output

### Verdict
Pass / Pass with polish / Revise / Block launch

### Delivery verification
Exactly where the test lead arrived.

### UX findings
Ranked by conversion impact.

### Accessibility findings
Ranked by severity.

### Analytics verification
Events confirmed and any gaps.

### Failure-path verification
What happens when the system fails.

### Remaining unknowns
Anything that could not be tested.