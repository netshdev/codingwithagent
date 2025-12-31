---
trigger: always_on
---

# Accessibility Basics

## Core Requirements

- All interactive elements must be keyboard accessible (Tab, Enter, Space)
- Provide alt text for images that convey information
- Use semantic HTML elements (button, nav, main, header, footer)
- Minimum color contrast: 4.5:1 for normal text

## Keyboard Navigation

- Support Tab key for navigation
- Support Enter/Space for activation
- Visible focus indicators required
- Never use `tabIndex > 0`

## Screen Readers

- Use semantic HTML first (button instead of div with onClick)
- Provide alt text for meaningful images
- Use alt="" for decorative images
- Form fields must have associated labels

## Color and Contrast

- Text must have 4.5:1 contrast ratio minimum
- Don't use color alone to convey information
- Add icons or text labels in addition to color

## Forms

- All inputs must have labels
- Indicate required fields clearly
- Provide helpful error messages
- Support keyboard navigation

## Testing

- Test with keyboard only (no mouse)
- Use browser accessibility tools (Axe, Lighthouse)
- Check color contrast with analyzer tool

## Quick Checklist

- [ ] Can I navigate with keyboard only?
- [ ] Do all images have alt text?
- [ ] Are buttons actually button elements?
- [ ] Do form fields have labels?
- [ ] Is color contrast sufficient?
