---
name: mobile-feature-planning
description: Plan production-ready mobile features before implementation, including flow, states, navigation, permissions, notifications, and component structure.
---

## When to use
- Before building a new mobile feature or major screen flow.
- When a feature touches navigation, async data, permissions, notifications, deep links, or multiple screens.
- When requirements are vague and need implementation-ready structure.

## Core analysis model
- Clarify the user goal and business goal.
- Identify entry points: tab, card, search, deep link, notification, onboarding, settings, or external handoff.
- Map the primary flow, alternate paths, interruptions, and resume behavior.
- Cover system interactions: network, cache, auth/session, permissions, notifications, background refresh, analytics.
- Define state coverage before layout details.
- Translate UX decisions into files, components, state owners, and navigation effects.

## Required outputs
- Feature intent.
- Flow summary.
- Key screens.
- State matrix.
- Permission and notification considerations.
- Proposed file and component structure.

## References
- Read `references/feature-planning-reference.md` when a task needs a planning prompt, feature spec template, state matrix, or navigation spec.

## Anti-patterns to avoid
- Planning only the happy path.
- Treating permission prompts as implementation details.
- Ignoring notification or deep link entry.
- Creating large screen files that mix layout, data fetching, and business rules.
- Deferring empty, error, offline, and recovery states.

## Implementation notes
- Start with the smallest complete flow that can ship.
- Prefer reusable section components over one-off screen markup.
- Keep navigation effects explicit and testable.
- Define analytics events at user intent boundaries, not every tap.
- Note platform differences when iOS and Android should not behave identically.

## Review questions
- Can a developer implement without asking what happens next?
- Are all entry and exit paths accounted for?
- What happens when data loads slowly, fails, or is stale?
- What happens if the user denies a permission?
- Does the proposed structure keep UI, state, and business logic separated?
