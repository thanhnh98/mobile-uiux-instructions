---
name: mobile-engineering-handoff
description: Translate mobile UX and UI decisions into maintainable code structure, component boundaries, state ownership, and implementation warnings.
---

## When to use
- After planning a feature and before coding.
- When converting specs or designs into implementation tasks.
- When a screen file risks becoming too large or stateful.

## Core analysis model
- Define the screen shell, route parameters, and navigation effects.
- Split sections, primitives, state renderers, and reusable components.
- Assign state ownership to UI, view model/controller, domain service, cache, or navigation.
- Identify events, analytics hooks, side effects, and async boundaries.
- Keep presentation components reusable and business logic centralized.
- Flag framework, platform, accessibility, and performance risks.

## Required outputs
- Suggested file structure.
- Component tree.
- State ownership notes.
- Event handling notes.
- Implementation warnings.

## Anti-patterns to avoid
- One screen file containing layout, fetching, validation, analytics, and navigation.
- Reusable components that know feature-specific business rules.
- Analytics buried inside low-level UI primitives.
- State renderers duplicated across screens.
- Navigation triggered from deeply nested presentational components.

## Implementation notes
- Prefer feature folders with screen, components, state/model, hooks/controllers, and tests.
- Keep component APIs small and named around user intent.
- Isolate platform-specific code behind narrow adapters where practical.
- Make retry, submit, cancel, and navigate events explicit.
- Add tests around state mapping and critical interaction flows.

## Review questions
- What code owns each state transition?
- Which components are feature-specific and which are reusable?
- Where do navigation and analytics side effects live?
- Can the screen be tested without real network or OS permissions?
- What implementation choice is most likely to age poorly?
