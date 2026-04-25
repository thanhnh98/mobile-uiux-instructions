# Production Review Reference

## Review Prompt Template

```text
Use the mobile-production-review, mobile-state-model, mobile-navigation-stack, mobile-permission-notification, mobile-accessibility, mobile-adaptive-layout, mobile-performance-ux, and mobile-engineering-handoff skills.

Review this mobile feature for production readiness:

Feature/screen:
[name and purpose]

Relevant files:
[paths]

Known concerns:
[bugs, UX issues, design drift, accessibility, state, navigation, platform behavior]

Review for:
- Missing or weak states
- Poor hierarchy or CTA conflicts
- Navigation and back behavior issues
- Deep link or notification entry risks
- Permission denial and settings recovery gaps
- Accessibility and dynamic text gaps
- Adaptive layout failures
- Performance UX issues in loading, lists, images, pagination, caching, or animation
- Implementation smells and test gaps

Return issues by severity with file references where possible, what to fix first, redesign direction, and release-readiness status.
```

## Production Review Checklist
- UX: user goal is clear, primary path is short and recoverable, empty/error/offline/blocked paths are useful.
- UI hierarchy: primary content and CTA are visually dominant, secondary actions do not compete, groups match decision sequence.
- States: initial, loading, success, empty, partial, error, offline, disabled, submitting, completed, and blocked states are covered where relevant.
- Navigation: entry points, back/up/close/dismiss behavior, deep links, notifications, stack duplication, and restore paths are handled.
- Permissions/notifications: request timing, denial, settings recovery, destination, and dedupe rules are defined.
- Accessibility: labels, roles, states, hints, focus order, dynamic text, gesture alternatives, and announcements are covered.
- Performance UX: first useful content, loading UI, long lists, images, refresh, retry, optimistic update, stale data, and animations are handled.
- Implementation quality: screen files stay thin, state ownership is explicit, side effects are isolated, and critical flows have tests or review notes.
- Adaptive behavior: small phones, large phones, tablets, keyboard, safe areas, landscape, or foldables are addressed when in scope.

