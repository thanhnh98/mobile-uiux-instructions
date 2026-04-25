# Production Review Checklist

## UX
- User goal is clear.
- Primary path is short and recoverable.
- Empty, error, offline, and blocked paths are useful.
- Copy is concise and action-oriented.

## UI Hierarchy
- Primary content and CTA are visually dominant.
- Secondary actions do not compete with primary actions.
- Content groups match the user decision sequence.
- Long content remains scannable.

## States
- Initial, loading, success, empty, partial, error, offline, disabled, submitting, completed, and blocked states are covered where relevant.
- Retry and recovery actions are clear.
- Duplicate submissions are prevented.
- Stale or deleted resources are handled.

## Navigation
- Entry points are defined.
- Back/up/close/dismiss behavior is platform-correct.
- Deep links and notification opens land in the right place.
- Stack duplication and broken restore paths are avoided.

## Permissions/Notifications
- Permission request timing is justified.
- Denied and blocked paths are usable.
- Settings recovery exists.
- Notifications have value, destination, and dedupe rules.

## Accessibility
- Controls have labels, roles, states, and hints.
- Focus order follows task order.
- Dynamic text and localization do not break layout.
- Gesture-only actions have alternatives.
- Status changes are announced.

## Performance UX
- First useful content appears quickly or cached content is shown.
- Loading UI matches final layout and avoids large jumps.
- Long lists use stable keys, pagination, and virtualization where needed.
- Images are correctly sized, cached, lazy-loaded, and cancelled when off-screen.
- Refresh, retry, optimistic update, and stale-data behavior are clear.
- Animations remain smooth and respect reduced motion.

## Implementation Quality
- Screen files stay thin.
- UI components do not own business rules.
- State ownership is explicit.
- Navigation and analytics side effects are isolated.
- Critical flows have tests or review notes.

## Adaptive Behavior
- Small phones are supported.
- Large phones and tablets do not merely stretch weak layouts.
- Keyboard and safe-area insets are handled.
- Landscape or foldables are addressed when in scope.
