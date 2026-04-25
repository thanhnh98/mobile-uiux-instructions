---
name: mobile-accessibility
description: Ensure mobile UI is accessible, operable, understandable, and resilient with assistive technologies.
---

## When to use
- For every new interactive mobile screen or component.
- When reviewing forms, lists, custom controls, gestures, animations, or state changes.
- When dynamic text, screen readers, or touch targets may affect usability.

## Core analysis model
- Verify tap target size and spacing.
- Define focus order and grouping.
- Add labels, roles, values, hints, and state semantics for interactive controls.
- Check contrast, icon-only controls, text scaling, reduced motion, and gesture alternatives.
- Announce loading, errors, completion, validation, and important state changes.
- Ensure custom components behave like native controls where possible.

## Required outputs
- Accessibility risks.
- Accessibility requirements.
- Required semantic labels.
- Adaptive text considerations.
- Remediation notes.

## References
- Read `references/accessibility-reference.md` when a task needs a checklist for labels, focus, contrast, text scaling, screen reader behavior, motion, gestures, or announcements.

## Anti-patterns to avoid
- Icon-only actions without accessible names.
- Custom gestures with no button or menu alternative.
- Truncated text under dynamic type.
- Color-only status indication.
- Focus order that follows implementation order instead of user task order.

## Implementation notes
- Prefer native controls before custom implementations.
- Mark decorative images as hidden from accessibility services.
- Combine or split screen reader groups based on decision usefulness.
- Keep labels stable and values dynamic for toggles, sliders, inputs, and progress.
- Respect reduced motion and avoid mandatory timed interactions.

## Review questions
- Can the screen be completed with a screen reader?
- Are all controls reachable and named?
- Does text scaling preserve meaning and action access?
- Are errors and status changes announced?
- Is every gesture-only action available another way?
