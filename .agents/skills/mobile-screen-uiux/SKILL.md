---
name: mobile-screen-uiux
description: Create or review a single mobile screen with production hierarchy, state coverage, accessibility, and implementation handoff.
---

## When to use
- When designing, implementing, or reviewing one mobile screen.
- When a screen needs clearer hierarchy, CTA priority, state handling, or component breakdown.
- When converting product requirements or Figma designs into code-ready UI.

## Core analysis model
- Define the screen intent and user context.
- Group content by task relevance, not source object shape.
- Establish information hierarchy and CTA priority.
- Choose fixed, sticky, and scrollable regions deliberately.
- Cover loading, empty, error, offline, partial, disabled, and submitting states.
- Check accessibility, dynamic text, safe areas, keyboard overlap, and small screens.
- Convert the screen into shell, sections, primitives, and state renderers.

## Required outputs
- Screen goal.
- Content blocks.
- Hierarchy recommendation.
- Layout structure.
- CTA strategy.
- State model.
- Accessibility notes.
- Component split suggestion.

## References
- Read `references/screen-uiux-reference.md` when a task needs a screen spec template, state matrix, accessibility checklist, or adaptive behavior notes.

## Anti-patterns to avoid
- Equal visual weight for every item.
- Multiple competing primary CTAs.
- Scroll views with hidden critical actions.
- Fixed footers that cover content or keyboard.
- Icon-only controls without labels.
- Screen files that own too many reusable pieces.

## Implementation notes
- Put the primary action where thumb reach, task timing, and platform convention align.
- Keep destructive or irreversible actions visually and behaviorally distinct.
- Use state renderer components when states have meaningfully different layouts.
- Prefer native controls for pickers, sheets, menus, inputs, and navigation where possible.

## Review questions
- Is the user’s next action obvious within three seconds?
- Does the screen remain usable with large text and long localized strings?
- Are all interactive elements labeled and reachable?
- Which areas scroll, which stay fixed, and why?
- Can the component split be reused by adjacent screens?
