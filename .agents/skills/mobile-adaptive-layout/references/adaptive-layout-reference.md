# Adaptive Layout Reference

Use these notes when a mobile screen must survive multiple device sizes, orientations, platform settings, localization, safe areas, and keyboard states.

## Device Classes
- Small phones: prioritize the primary task, avoid fixed heights, and allow vertical scrolling.
- Large phones: use extra space for breathing room or secondary context, not unrelated decoration.
- Tablets and foldables: consider multi-pane layouts only when they improve task flow.
- Landscape: reduce vertical chrome and keep the primary action reachable.

## Safe Areas and Insets
- Respect notches, home indicators, status bars, navigation bars, and gesture regions.
- Bottom CTAs should sit above system gesture areas and not cover scroll content.
- Edge-to-edge layouts need explicit contrast and inset handling.

## Keyboard
- Inputs and primary actions must remain reachable when the keyboard is open.
- Forms should scroll to focused fields and preserve context.
- Avoid fixed footers that overlap text fields or validation errors.
- Support hardware keyboard and return-key behavior where relevant.

## Localization and Text Scaling
- Test long strings in headers, tabs, buttons, cards, and empty states.
- Prefer wrapping, scrolling, or reflowing over clipping.
- Dynamic text should preserve action access and meaning.

## Accessibility Settings
- Respect dynamic type/font scale, bold text, reduce motion, high contrast, and touch accommodations.
- Provide alternate layouts when large text would make a dense layout unusable.

