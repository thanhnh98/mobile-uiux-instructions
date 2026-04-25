---
name: mobile-navigation-stack
description: Design and review mobile navigation, stack behavior, deep links, notification entry, and platform-correct exits.
---

## When to use
- When adding or changing a flow with push, modal, sheet, tab, or nested navigation.
- When supporting deep links, push notifications, auth gates, or restore/resume behavior.
- When back, up, close, dismiss, or exit behavior could be ambiguous.

## Core analysis model
- Classify the flow as top-level, nested, modal, transient sheet, or external handoff.
- Define entry points and required context for each entry.
- Choose push vs modal vs sheet based on task ownership and exit expectations.
- Specify back, up, close, dismiss, cancel, and completion behavior.
- Handle deep link and notification entry without corrupting the stack.
- Account for restore/resume, auth/session expiry, and missing resources.

## Required outputs
- Entry points.
- Navigation model.
- Back behavior.
- Exit paths.
- Stack risks.
- Platform notes.

## References
- Read `references/navigation-stack-reference.md` when a task needs a navigation spec template, deep link handling, notification entry behavior, restore behavior, or platform-specific back behavior.

## Anti-patterns to avoid
- Using modals for long multi-step flows without clear dismissal rules.
- Breaking native back gestures.
- Sending notification users to a generic landing screen.
- Creating duplicate screens on repeated deep links.
- Losing user progress on app background/resume.

## Implementation notes
- Keep navigation effects out of pure presentation components.
- Centralize route parameters and validate required IDs before rendering.
- Prefer idempotent deep link handling.
- Document differences between Android back, iOS swipe back, close buttons, and sheet dismissal.

## Review questions
- What stack should exist after each entry point?
- What happens when the user presses system back?
- What happens after completion, cancellation, or auth failure?
- Can the same destination be opened twice incorrectly?
- Does platform behavior feel native?
