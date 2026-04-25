# Navigation Stack Reference

## Navigation Spec Template

## Entry Points
- Top-level entry:
- Nested entry:
- Deep link:
- Push notification:
- External handoff:

## Navigation Path
- Start route:
- Intermediate routes:
- Destination route:
- Required route params:
- Auth or data prerequisites:

## Back Behavior
- Header back/up:
- System back:
- Gesture back:
- After completion:
- After cancellation:

## Modal/Sheet Rules
- Presentation type:
- Dismiss behavior:
- Unsaved changes:
- Drag-to-dismiss:
- Platform differences:

## Deep Link Behavior
- Valid link:
- Missing resource:
- Unauthorized user:
- Existing stack:
- Duplicate destination prevention:

## Notification Entry Behavior
- Destination:
- Stale notification:
- Already-open destination:
- Missing permission/session:
- Fallback route:

## Restore Behavior
- App resume:
- Process restart:
- Interrupted flow:
- Expired data:
- Offline restore:

## Platform Notes
- iOS commonly uses tab bars for top-level areas, navigation stacks for drill-in flows, swipe-back gestures, and modal presentation for temporary or self-contained tasks.
- Android commonly uses bottom navigation for top-level areas, explicit app bars for hierarchy, system back behavior, and task-aware activity/navigation stacks.
- Cross-platform apps should preserve each platform's back expectations instead of forcing one shared mental model.

