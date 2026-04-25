# Mobile Platform Notes

Use these notes when a feature must feel native on both iOS and Android. Prefer platform conventions unless the product has a documented reason to diverge.

## Navigation
- iOS commonly uses tab bars for top-level areas, navigation stacks for drill-in flows, swipe-back gestures, and modal presentation for temporary or self-contained tasks.
- Android commonly uses bottom navigation for top-level areas, explicit app bars for hierarchy, system back behavior, and task-aware activity/navigation stacks.
- Cross-platform apps should preserve each platform's back expectations instead of forcing one shared mental model.
- Deep links and notification entry should land on the most specific useful screen, with fallback for missing auth, missing resource, or stale context.

## Modals and Sheets
- iOS sheets should feel dismissible only when dismissal is safe; protect unsaved changes.
- Android bottom sheets should have clear collapsed, expanded, and dismissed behavior when used.
- Use full-screen modal flows for focused tasks that temporarily take over the experience.
- Avoid nesting modals or using sheets for long, multi-step flows.

## Permissions
- Ask at the moment of user intent when possible.
- Explain value before system prompts if denial would block the task.
- Support denied, blocked, limited, and settings-recovery paths.
- iOS and Android permission states can differ; do not assume a single boolean permission model.

## Back Behavior
- Android system back must be predictable and should not exit a flow unexpectedly.
- iOS swipe back should remain available unless blocking protects user work.
- Use close/dismiss for modal tasks and back/up for hierarchical navigation.
- After completion, define whether the user returns, lands on a result, or exits the flow.

## Safe Areas and Insets
- Respect notches, home indicators, status bars, navigation bars, and gesture regions.
- Bottom CTAs should sit above system gesture areas and not cover scroll content.
- Edge-to-edge layouts need explicit contrast and inset handling.
- Test devices with different cutouts and navigation modes.

## Keyboard
- Inputs and primary actions must remain reachable when the keyboard is open.
- Forms should scroll to focused fields and preserve context.
- Avoid fixed footers that overlap text fields or validation errors.
- Support hardware keyboard and return-key behavior where relevant.

## Notifications
- Notification copy should communicate value and expected destination.
- Tapping a notification should route to the specific item or task, not a generic home screen.
- Handle stale notifications, logged-out users, missing resources, and duplicate taps.
- Cancel, replace, or group notifications when repeated events would create noise.

## Accessibility
- iOS VoiceOver and Android TalkBack may expose grouping, order, and actions differently; test both when cross-platform.
- Use platform-native controls for expected semantics when possible.
- Provide labels for icon-only controls, state values for toggles/progress, and announcements for important status changes.
- Respect dynamic type/font scale, bold text, reduce motion, high contrast, and touch accommodations.

## Review Checklist
- Does each platform's back behavior match user expectations?
- Are system prompts timed around user intent?
- Are safe areas, keyboard, and gesture regions handled?
- Do notification and deep link entries restore the right stack?
- Can the feature be completed with VoiceOver or TalkBack?
