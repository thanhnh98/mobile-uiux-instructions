# Mobile UI/UX Engineering Instructions

Treat mobile UI work as production product work, not visual decoration. For every mobile feature, reason from the user goal, business goal, hierarchy, state coverage, navigation path, accessibility, and implementation feasibility before coding.

Keep screen files thin. Split reusable UI into focused components, keep state orchestration close to the screen or feature boundary, and keep business logic out of presentation-only components.

For new feature screens, include loading, empty, error, offline, disabled, submitting, and recovery states where relevant. Do not ship happy-path-only UI.

Respect platform-native behavior for iOS, Android, and cross-platform frameworks: navigation gestures, modals, sheets, safe areas, keyboard handling, permissions, notification entry, deep links, and accessibility services.

When permissions, notifications, or navigation side effects are involved, define the request timing, denial path, settings recovery, entry destination, back behavior, and stack implications.

Add accessibility labels, roles, semantics, focus order, state announcements, and gesture alternatives for interactive elements where applicable. Support dynamic text and small screens.

For complex UI features, write a concise plan before implementation. Prefer practical artifacts: state matrix, navigation notes, component tree, and release risks.
