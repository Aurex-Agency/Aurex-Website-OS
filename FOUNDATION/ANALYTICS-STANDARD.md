# Aurex Analytics Standard

Aurex websites should generate useful evidence about business outcomes without turning every click into noise.

Analytics exists to answer business questions, improve conversion, diagnose journeys, and evaluate marketing. Tracking more events is not automatically better measurement.

## 1. Start with business outcomes

Before implementation, define:

- primary conversion
- secondary conversions
- meaningful funnel steps
- qualified-lead definition when known
- downstream outcomes available from CRM or sales systems

Tracking should map to those outcomes.

## 2. Event taxonomy

Use clear, stable event names.

Prefer names that communicate business meaning such as:

- lead_form_start
- lead_form_submit
- appointment_booked
- phone_click
- sms_click
- directions_click
- financing_start
- financing_complete
- product_inquiry_submit

Avoid vague events such as `button_click_3`.

## 3. Event payloads

Include context that supports analysis without sending sensitive or unnecessary personal data.

Useful context may include:

- page type
- service/category
- location
- form type
- CTA placement
- traffic source where analytics already provides it

Do not place names, phone numbers, emails, form messages, health details, financial details, or other sensitive information in analytics payloads.

## 4. Form funnels

When a form is strategically important, consider measuring:

- form view when meaningful
- form start
- step progression for multi-step flows
- validation/error friction where useful
- submission
- qualified lead or booking when downstream data exists

Do not create dozens of step events unless the data will actually be reviewed.

## 5. Conversion platform alignment

Where applicable, ensure key business conversions reach the platforms that need them, which may include:

- GA4
- Google Ads
- Meta
- CRM
- call tracking
- scheduling platform
- internal notifications

Do not assume one analytics tool automatically handles advertising conversion attribution correctly.

## 6. Duplicate prevention

Conversion events should not accidentally fire multiple times because of rerenders, route transitions, back navigation, retries, or thank-you page refreshes.

Use idempotent event behavior where appropriate.

## 7. Consent and privacy

Analytics and advertising implementations must respect the project's consent and privacy requirements.

Do not make legal assumptions about what tracking is permitted in a jurisdiction or industry.

Implement the client's approved consent strategy and escalate unresolved legal questions.

## 8. Debugging

Before launch:

- test events in browser debugging tools
- verify correct event names and parameters
- verify platform receipt where possible
- test both successful and failed form paths
- verify events are not firing on page load when they represent a conversion
- verify redirects do not lose the event
- verify cross-domain flows when applicable

## 9. Post-launch measurement

When enough data exists, report:

- conversion rate by important landing page
- lead volume and quality when available
- form completion and abandonment
- device differences
- traffic-source differences
- page groups that assist conversion
- SEO landing pages that generate business outcomes

Avoid overinterpreting tiny sample sizes.

## 10. Measurement integrity

Aurex should distinguish between:

- tracked event
- confirmed lead
- qualified lead
- appointment
- sale/revenue

Do not call a button click a lead or a form start a conversion.

The closer measurement gets to actual business outcomes, the more useful the website becomes as a growth system.