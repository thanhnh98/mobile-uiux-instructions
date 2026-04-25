---
name: mobile-permission-notification
description: Plan and review permission prompts and notification UX as part of production mobile flows.
---

## When to use
- When a feature needs camera, photo library, location, contacts, Bluetooth, microphone, notifications, tracking, health, or storage access.
- When adding push, local notifications, reminders, alerts, or notification-driven navigation.
- When denied, blocked, or settings recovery paths affect completion.

## Core analysis model
- Explain why the permission is needed and what user value it unlocks.
- Choose when to ask: at intent, setup, onboarding, or just-in-time.
- Decide whether pre-permission education is needed.
- Define granted, denied, blocked, limited, and settings recovery paths.
- Clarify notification value, timing, frequency, destination, and duplicate prevention.
- Account for platform permission differences and OS settings behavior.

## Required outputs
- Permission strategy.
- Notification strategy.
- Settings fallback.
- UX copy intent notes.
- Edge cases.

## References
- Read `references/permission-notification-reference.md` when a task needs permission states, ask timing, settings recovery, notification destination, dedupe, or stale notification handling.

## Anti-patterns to avoid
- Asking for permission before the user understands the value.
- Treating denial as an error state only.
- Dead-ending blocked users without settings recovery.
- Sending notifications with no clear destination.
- Triggering duplicate or stale notifications.

## Implementation notes
- Request permissions from explicit user intent when possible.
- Keep copy short and benefit-led; avoid manipulative language.
- Store notification IDs where cancellation or dedupe is required.
- Route notification opens to the most specific useful destination with fallback handling.
- Handle limited photo/location permissions where supported.

## Review questions
- Why is the permission needed now?
- What can the user still do if they deny it?
- Is there a clear settings recovery path?
- Where does each notification open?
- How are stale, duplicate, or unauthorized notification entries handled?
