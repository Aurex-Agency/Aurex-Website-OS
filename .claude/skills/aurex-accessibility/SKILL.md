---
name: aurex-accessibility
description: Audits and improves an Aurex website against WCAG 2.2 AA using automated scans plus manual keyboard, focus, form, motion, semantic, and interaction review. Use during QA and when implementing complex interactions.
---

# Aurex Accessibility Review

Use `FOUNDATION/ACCESSIBILITY-STANDARD.md`.

Automated scans are assistance, not certification.

## 1. Select representative experiences

Include:

- homepage
- primary content/service template
- primary conversion flow
- navigation
- any modal/menu/custom control
- any complex animation
- a long-form page when relevant

## 2. Automated scan

If Playwright + axe or another configured tool exists, run it against representative routes and interactive states.

Record violations by severity and page pattern.

Do not assume zero automated violations means accessible.

## 3. Keyboard walkthrough

Using keyboard only:

- enter page
- skip repeated navigation when supported
- navigate header/menu
- reach all primary controls
- operate accordions/tabs/dialogs/carousels
- complete the primary form
- close overlays
- verify logical focus return

Check focus visibility and whether sticky/floating content obscures focus.

## 4. Forms

Verify:

- labels
- instructions
- autocomplete
- required state
- errors
- focus on invalid input where appropriate
- status/success communication
- touch targets

## 5. Visual accessibility

Check:

- text contrast
- UI/control contrast
- information not communicated through color alone
- zoom/text resizing does not destroy functionality
- target sizing and spacing
- reading order

## 6. Motion

Enable reduced motion and verify:

- content remains available
- page does not require animated state to make sense
- parallax/large movement is removed or simplified
- focus and navigation do not depend on smooth scrolling

## 7. Media

Review alt text purpose, decorative images, captions/transcripts where required, and autoplay behavior.

## 8. Fix systemic issues first

If the same violation comes from a shared primitive, fix the primitive rather than patching every page.

## Output

### Verdict
Pass / Pass with important fixes / Revise / Block launch

### Automated findings
Tool used and issues found.

### Manual findings
Keyboard, focus, forms, semantics, motion, media.

### Systemic fixes
Shared components that should be corrected once.

### Remaining manual risk
What cannot be established automatically.

Do not claim formal WCAG conformance unless the required audit scope and evidence actually support that claim.