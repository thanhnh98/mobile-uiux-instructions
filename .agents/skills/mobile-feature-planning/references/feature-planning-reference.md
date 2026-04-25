# Feature Planning Reference

## Plan Prompt Template

```text
Use the mobile-feature-planning, mobile-state-model, mobile-navigation-stack, mobile-permission-notification, mobile-accessibility, mobile-adaptive-layout, mobile-performance-ux, and mobile-engineering-handoff skills.

Plan this mobile feature for production implementation:

Feature:
[describe the feature]

Target platform/framework:
[iOS / Android / React Native / Flutter / Kotlin Multiplatform / other]

Known requirements:
[list requirements]

Constraints:
[API, design system, navigation, auth, analytics, deadlines]

Produce:
- Feature intent
- Flow summary
- Key screens
- State matrix
- Navigation model
- Permission/notification considerations
- Accessibility and adaptive layout risks
- Performance UX risks
- Proposed file/component structure
- Implementation warnings

Keep the plan concise and implementation-ready. Do not write code yet unless explicitly asked.
```

## Feature Spec Template

- Feature intent: what is being shipped, why now, success definition.
- User goal: primary user, job to complete, main constraint or concern.
- Business goal: outcome, metric or signal, non-goals.
- Entry points: primary, secondary, deep link, notification.
- Flow: start, main path, alternate paths, completion, exit/cancel.
- Interruptions: background/resume, network loss, auth expiry, incoming notification, partial progress recovery.
- States: initial, loading, success, empty, partial, error, offline, disabled/blocked, submitting/completed.
- Permission/notification: needed access, ask timing, denied/blocked behavior, settings recovery, value, destination, duplicate/stale prevention.
- Analytics: opened, primary action, failure/retry, completion, drop-off points.
- Implementation notes: suggested files, component boundaries, state owner, navigation effects, platform differences, test focus.

## State Matrix Template

| State | Visible UI | Enabled Actions | Side Effects | Recovery Path |
| --- | --- | --- | --- | --- |
| Initial |  |  |  |  |
| Loading |  |  |  |  |
| Success |  |  |  |  |
| Empty |  |  |  |  |
| Partial |  |  |  |  |
| Error |  |  |  |  |
| Offline |  |  |  |  |
| Disabled |  |  |  |  |
| Submitting |  |  |  |  |
| Completed |  |  |  |  |
| Permission denied |  |  |  |  |
| Permission blocked |  |  |  |  |
| Session expired |  |  |  |  |
| Stale/deleted resource |  |  |  |  |

## Navigation Spec Template

- Entry points: top-level entry, nested entry, deep link, push notification, external handoff.
- Navigation path: start route, intermediate routes, destination route, route params, auth/data prerequisites.
- Back behavior: header back/up, system back, gesture back, after completion, after cancellation.
- Modal/sheet rules: presentation type, dismiss behavior, unsaved changes, drag-to-dismiss, platform differences.
- Deep link behavior: valid link, missing resource, unauthorized user, existing stack, duplicate destination prevention.
- Notification entry behavior: destination, stale notification, already-open destination, missing permission/session, fallback route.
- Restore behavior: app resume, process restart, interrupted flow, expired data, offline restore.

