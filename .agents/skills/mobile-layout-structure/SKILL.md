---
name: mobile-layout-structure
description: Analyze or propose mobile layout composition for resilient scrolling, sticky regions, keyboard handling, and small-screen survival.
---

## When to use
- When a screen layout feels crowded, fragile, or unclear.
- When deciding between list, form, detail, feed, dashboard, wizard, or tool layouts.
- When keyboard, sticky actions, long content, or small devices affect usability.

## Core analysis model
- Pick the layout archetype that matches the user task.
- Group sections by scanning order and decision sequence.
- Define spacing rhythm, density, and visual breaks.
- Decide which regions are fixed, sticky, collapsible, or scrollable.
- Test long content, keyboard overlap, dynamic text, safe areas, and small phones.
- Preserve primary actions without hiding content or blocking system gestures.

## Required outputs
- Layout type.
- Section breakdown.
- Sticky/fixed rules.
- Scrolling behavior.
- Adaptation rules.
- Layout risks.

## References
- Read `references/layout-structure-reference.md` when a task needs a screen structure template, fixed-area rules, keyboard behavior, safe-area guidance, or adaptive layout notes.

## Anti-patterns to avoid
- Nested scroll areas without a strong reason.
- Sticky headers or footers that consume too much vertical space.
- Layouts that only work on large phones.
- Hard-coded heights for dynamic content.
- Treating forms, feeds, and detail pages as the same structure.

## Implementation notes
- Prefer intrinsic sizing, constraints, and platform layout primitives over fixed dimensions.
- Use safe-area and keyboard-aware containers for bottom actions and inputs.
- Keep repeated item rows stable under long text and loading placeholders.
- Make overflow behavior explicit for every section.

## Review questions
- What is the layout archetype and why?
- Does the screen survive the smallest supported device?
- Can users complete the task with the keyboard open?
- Are sticky areas helping completion or reducing usable space?
- What content can collapse, truncate, or move when space is constrained?
