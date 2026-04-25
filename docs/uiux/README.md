# Mobile UI/UX Instruction System

This directory contains reusable templates and checklists for planning, building, and reviewing production mobile UI/UX work with an AI coding assistant.

`AGENTS.md` sets repository-wide behavior: mobile-first reasoning, complete state coverage, native platform behavior, accessibility, and implementation-ready structure.

## Skills
- `mobile-feature-planning`: plan a full feature flow before coding.
- `mobile-screen-uiux`: design or review one screen.
- `mobile-layout-structure`: choose resilient layout composition.
- `mobile-state-model`: define state variants, actions, and recovery.
- `mobile-navigation-stack`: handle stack, modal, back, deep link, and notification entry.
- `mobile-permission-notification`: plan permission and notification UX.
- `mobile-accessibility`: verify accessible operation.
- `mobile-adaptive-layout`: support sizes, orientation, localization, keyboard, and safe areas.
- `mobile-performance-ux`: improve perceived performance, list rendering, media loading, caching, and responsiveness.
- `mobile-engineering-handoff`: turn UX decisions into component and file structure.
- `mobile-production-review`: review readiness before release.

## Workflows
- Plan: use `plan-prompt-template.md`, then fill `feature-spec-template.md`, `state-matrix-template.md`, and `navigation-spec-template.md`.
- Build: use `build-prompt-template.md`, then keep the implementation aligned with `screen-spec-template.md`.
- Review: use `review-prompt-template.md`, then check against `production-review-checklist.md`, `accessibility-checklist.md`, and `mobile-platform-notes.md`.

Keep outputs short, specific, and tied to implementation decisions.
