---
name: mobile-state-model
description: Define complete UI state systems for mobile screens and features, including recovery paths and state ownership.
---

## When to use
- Before implementing async, form, permission, payment, sync, or account-dependent UI.
- When reviewing a screen that handles loading, empty data, errors, offline use, or blocked access.
- When state ownership between UI and business logic is unclear.

## Core analysis model
- Enumerate initial, loading, success, empty, partial, error, offline, disabled, submitting, completed, and blocked states.
- Add denied permission, stale data, deleted resource, and session-expired states when relevant.
- Define visible UI, enabled actions, side effects, and recovery path per state.
- Decide which state belongs in UI, view model/controller, cache, navigation, or domain layer.
- Prevent impossible state combinations.

## Required outputs
- State matrix.
- State-specific UI behavior.
- Allowed actions per state.
- Retry or recovery path.
- Ownership of state between UI and business logic.

## References
- Read `references/state-model-reference.md` when a task needs a complete state matrix template or guidance for visible UI, actions, side effects, and recovery paths.

## Anti-patterns to avoid
- Loading spinners without timeout, skeleton, or retry behavior.
- Empty states that do not tell users what action is possible.
- Error messages with no recovery.
- UI components making business-state decisions independently.
- Submitting states that allow duplicate actions.

## Implementation notes
- Model states as explicit variants where the framework supports it.
- Keep state names user-meaningful and implementation-testable.
- Disable or debounce actions during submission and navigation transitions.
- Use cached or partial UI carefully; mark stale data when it affects decisions.

## Review questions
- Are all async outcomes represented?
- What actions are enabled in each state?
- Can the user recover without restarting the app?
- Who owns each state transition?
- Are there impossible combinations that should be prevented by the model?
