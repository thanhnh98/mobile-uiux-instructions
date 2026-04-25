# Permission and Notification Reference

## Permissions
- Ask at the moment of user intent when possible.
- Explain value before system prompts if denial would block the task.
- Support granted, denied, blocked, limited, and settings-recovery paths.
- iOS and Android permission states can differ; do not assume a single boolean permission model.

## Permission Spec
- Permission needed:
- User value unlocked:
- Ask timing:
- Pre-permission education:
- Granted behavior:
- Denied behavior:
- Blocked behavior:
- Limited access behavior:
- Settings recovery:
- What remains usable without permission:

## Notifications
- Notification copy should communicate value and expected destination.
- Tapping a notification should route to the specific item or task, not a generic home screen.
- Handle stale notifications, logged-out users, missing resources, and duplicate taps.
- Cancel, replace, or group notifications when repeated events would create noise.

## Notification Spec
- Notification value:
- Trigger timing:
- Frequency:
- Destination:
- Fallback destination:
- Dedupe key:
- Stale notification behavior:
- Missing permission/session behavior:
- Cancellation or replacement rules:

