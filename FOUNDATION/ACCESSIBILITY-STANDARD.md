# Aurex Accessibility Standard

Accessibility is part of premium execution. Aurex should target WCAG 2.2 AA for new marketing websites unless a project has a stronger contractual or legal requirement.

Automated tooling is useful but incomplete. Accessibility requires both automated checks and human interaction review.

## 1. Semantic structure

Use native HTML elements whenever they correctly represent the interaction or content.

Prefer:

- buttons for actions
- anchors for navigation
- headings in a logical hierarchy
- landmarks such as header, nav, main, aside, and footer
- lists for actual lists
- labels associated with form controls
- tables only for tabular data

Do not recreate native controls with generic divs unless there is a compelling reason and the full accessibility behavior is implemented.

## 2. Keyboard access

Every interactive feature must be usable without a mouse.

Verify:

- logical focus order
- visible focus indication
- no keyboard traps
- menus can open and close predictably
- dialogs manage focus correctly
- accordions, tabs, carousels, and custom controls follow appropriate keyboard patterns
- skip navigation is available when useful
- sticky elements do not entirely obscure focused controls

## 3. Focus

Never remove focus outlines without providing an equal or better visible replacement.

Focused elements should remain visible and should not be hidden by sticky headers, cookie banners, floating chat controls, or other author-created overlays.

Aurex should generally use focus styles that are easier to see than the minimum requirement.

## 4. Color and contrast

Do not rely on color alone to communicate status, selection, errors, or required actions.

Check text and UI contrast against WCAG requirements.

Brand colors may need adjusted variants for text, interactive states, or dark/light surfaces.

Do not sacrifice readability to preserve an exact brand hex value.

## 5. Target size and touch

Design controls for comfortable touch use.

WCAG 2.2 AA includes a 24 by 24 CSS pixel minimum target requirement with defined exceptions. Aurex should generally aim larger for primary controls and mobile interactions.

Do not place tiny adjacent icon controls where mistaps are likely.

## 6. Forms

Forms require:

- persistent or programmatically associated labels
- clear required-state communication
- useful instructions before errors occur when needed
- error messages that identify the problem
- error association with the relevant field
- keyboard-friendly completion
- correct autocomplete values when applicable
- input types appropriate to the requested information
- accessible success and status messages

Do not use placeholder text as the only label.

## 7. Images and media

Write alternative text based on purpose, not file contents.

Decorative images should not create noise for assistive technology.

Complex informative visuals may require nearby explanation beyond short alt text.

Videos with meaningful spoken content should have captions or equivalent accessible content as appropriate.

Avoid autoplaying audio.

## 8. Motion

Respect `prefers-reduced-motion`.

When reduced motion is requested:

- remove non-essential parallax
- remove unnecessary scale/translation choreography
- replace complex reveals with simple state changes
- avoid forced smooth scrolling
- keep content immediately available

Do not make comprehension depend on animation.

## 9. Hover and pointer interactions

Do not make essential content or functionality available only on hover.

Interactions should work across mouse, keyboard, touch, and assistive technologies where relevant.

Provide a non-drag alternative when a control depends on dragging and dragging is not essential.

## 10. Navigation and orientation

Navigation labels should be understandable.

Maintain consistent navigation patterns across the site.

Do not restrict the site to one device orientation unless essential.

## 11. Modals and overlays

Dialogs must:

- expose correct semantics
- move focus appropriately when opened
- keep focus within the modal when required
- close through an obvious control
- normally support Escape where appropriate
- return focus sensibly after closing
- avoid trapping screen-reader or keyboard users behind the overlay

## 12. Automated testing

For projects with automated browser tests, use Playwright with axe or an equivalent respected accessibility engine to detect common violations.

Automated scans do not prove WCAG conformance.

They must be complemented by manual checks for:

- keyboard flow
- focus visibility
- page structure
- labels and instructions
- visual reading order
- interaction clarity
- reduced motion
- error recovery

## 13. Manual representative-page review

At minimum, manually review representative templates including:

- homepage
- primary service/product template
- conversion/contact flow
- location page when used
- long-form/content page when used
- any page with complex animation or custom interaction

## 14. Accessibility and creativity

Accessibility does not require bland design.

When a creative idea conflicts with usability, redesign the implementation rather than abandoning either the concept or the user.

The best Aurex work should feel more intentional because accessibility was considered, not less distinctive.