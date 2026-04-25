---
name: mobile-adaptive-layout
description: Make mobile screens work across small phones, large phones, tablets, foldables, landscape, localization, keyboard, and safe-area contexts.
---

## When to use
- When implementing layouts that must support multiple device sizes or orientations.
- When a screen includes long text, forms, maps, media, grids, or side-by-side content.
- When tablet, foldable, landscape, localization, or keyboard behavior is in scope.

## Core analysis model
- Define behavior for small phones, large phones, tablets, and foldables when relevant.
- Choose size-class or breakpoint behavior.
- Prioritize content when vertical or horizontal space is constrained.
- Plan safe area, inset, keyboard, split-screen, and orientation behavior.
- Account for localization growth and dynamic text.
- Define fallback layouts rather than letting constraints fail.

## Required outputs
- Adaptation rules.
- Breakpoints or size-class behavior notes.
- Content priority for constrained space.
- Layout fallback behavior.

## References
- Read `references/adaptive-layout-reference.md` when a task needs platform notes for safe areas, keyboard behavior, orientation, tablets, foldables, localization, or accessibility settings.

## Anti-patterns to avoid
- Assuming one phone size.
- Fixed grids that overflow under localization or text scaling.
- Bottom actions hidden by keyboard or gesture areas.
- Tablet layouts that merely stretch phone UI.
- Landscape layouts with unusable vertical density.

## Implementation notes
- Use platform size classes, window metrics, or responsive constraints.
- Prefer one-column phone layouts and multi-pane tablet layouts only when they improve task flow.
- Keep essential actions visible or reachable when the keyboard is open.
- Test long localized strings in buttons, tabs, headers, and cards.

## Review questions
- What changes on the smallest supported phone?
- What changes on tablet or wide screens?
- What content loses priority first?
- Does keyboard entry block the task?
- Are safe areas and system gesture regions respected?
