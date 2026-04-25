# Layout Structure Reference

## Screen Spec Template

- Screen goal: user intent, screen outcome, required context.
- Primary CTA: primary action, secondary actions, disabled/submitting behavior, destructive action handling.
- Content groups: header/context, primary content, supporting content, metadata, empty/helper content.
- Hierarchy: most important information, scan order, visual priority, items to de-emphasize.
- Layout type: archetype, section order, density, spacing rhythm.
- Fixed areas: sticky header, bottom action, floating action, keyboard-aware behavior.
- State coverage: loading, success, empty, error, offline, partial/stale, permission denied/blocked.
- Accessibility: labels, focus order, announcements, gesture alternatives, dynamic text risks.
- Adaptive behavior: small phone, large phone, tablet/wide, landscape, localization growth, safe area/insets.
- Component split: screen shell, sections, reusable primitives, state renderers, feature-specific components.

## Sticky and Scroll Rules
- Use one primary scroll container unless a nested scroll region is essential.
- Sticky regions should improve task completion, not simply preserve decoration.
- Bottom actions must not cover content, validation errors, or system gesture areas.
- Keyboard-open states must keep the focused field and relevant action reachable.

## Safe Area and Keyboard Notes
- Respect notches, home indicators, status bars, navigation bars, and gesture regions.
- Forms should scroll to focused fields and preserve context.
- Avoid fixed heights for dynamic content.

