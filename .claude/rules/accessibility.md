---
paths:
  - "**/*.{ts,tsx,js,jsx,html,css,scss}"
---

# Accessibility Implementation Rules

- Target WCAG 2.2 AA for new Aurex marketing websites unless a stronger requirement applies.
- Prefer native semantic HTML over recreated controls.
- Buttons perform actions. Links navigate.
- Interactive controls must be keyboard operable and have visible focus states.
- Sticky headers, banners, floating CTAs, and overlays must not completely hide focused controls.
- Forms need programmatically associated labels, understandable errors, useful instructions, and accessible success/status feedback.
- Placeholder text cannot be the only form label.
- Use appropriate input types and autocomplete attributes.
- Do not rely on color alone for status, selection, errors, or required information.
- Check text and UI contrast. Adjust brand colors for accessible use when necessary.
- Touch targets must meet WCAG minimum requirements and should usually be larger for important mobile actions.
- Essential content cannot require hover.
- Provide a non-drag alternative when dragging is not essential.
- Modals must manage focus and close predictably.
- Meaningful images need purpose-based alt text. Decorative images should not create screen-reader noise.
- Respect reduced-motion preferences and keep the page fully understandable without non-essential animation.
- Automated axe/Lighthouse checks are not proof of accessibility. Manually test keyboard flow, focus, forms, menus, dialogs, reduced motion, and representative page structure.