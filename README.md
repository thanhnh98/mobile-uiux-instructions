# Mobile UI/UX Instructions

A Codex skill pack for planning, building, and reviewing production-grade mobile UI/UX work.

This repository is structured for publication as a skill repository. It provides focused mobile UX skills under `.agents/skills` and reusable planning/review artifacts under `docs/uiux`.

## What this pack covers

- Production mobile feature planning before implementation.
- Single-screen UI/UX hierarchy, layout, state, and accessibility review.
- Complete state modeling for loading, empty, error, offline, disabled, submitting, blocked, and recovery states.
- Native mobile navigation behavior for stack, modal, sheet, deep link, notification, and back handling.
- Permission and notification UX timing, denial paths, settings recovery, and entry destinations.
- Accessibility, adaptive layout, performance UX, engineering handoff, and release readiness review.

## Repository structure

```text
.
├── AGENTS.md
├── README.md
├── .agents/
│   └── skills/
│       ├── mobile-accessibility/
│       ├── mobile-adaptive-layout/
│       ├── mobile-engineering-handoff/
│       ├── mobile-feature-planning/
│       ├── mobile-layout-structure/
│       ├── mobile-navigation-stack/
│       ├── mobile-performance-ux/
│       ├── mobile-permission-notification/
│       ├── mobile-production-review/
│       ├── mobile-screen-uiux/
│       └── mobile-state-model/
└── docs/
    └── uiux/
        ├── README.md
        ├── *-template.md
        └── *-checklist.md
```

Each skill folder contains:

- `SKILL.md`: required agent-facing workflow and trigger instructions.
- `agents/openai.yaml`: UI metadata for skill listings and default prompts.

## Skills

| Skill | Use it for |
| --- | --- |
| `mobile-feature-planning` | Planning a complete mobile feature flow before coding. |
| `mobile-screen-uiux` | Creating or reviewing one mobile screen. |
| `mobile-layout-structure` | Designing resilient scrolling, sticky, keyboard, and small-screen layout behavior. |
| `mobile-state-model` | Defining UI states, allowed actions, ownership, and recovery paths. |
| `mobile-navigation-stack` | Reviewing push, modal, sheet, tab, deep link, notification, and back behavior. |
| `mobile-permission-notification` | Planning permission prompts, denial handling, settings recovery, and notifications. |
| `mobile-accessibility` | Checking labels, roles, focus, dynamic text, touch targets, and gesture alternatives. |
| `mobile-adaptive-layout` | Supporting phone sizes, tablets, foldables, orientation, localization, keyboard, and safe areas. |
| `mobile-performance-ux` | Improving perceived loading, list performance, media loading, caching, and interaction responsiveness. |
| `mobile-engineering-handoff` | Turning UX decisions into component structure, state ownership, and implementation warnings. |
| `mobile-production-review` | Reviewing release readiness across UX, state, navigation, accessibility, platform behavior, and code structure. |

## Usage

Invoke a skill explicitly in Codex with `$skill-name`.

Examples:

```text
Use $mobile-feature-planning to plan a production-ready booking flow for a mobile app.
```

```text
Use $mobile-screen-uiux to review this checkout screen for hierarchy, states, accessibility, and implementation handoff.
```

```text
Use $mobile-production-review to review this mobile feature before release.
```

## Supporting docs

The `docs/uiux` directory contains reusable artifacts for teams:

- Planning prompts and feature spec templates.
- Build prompt and screen spec templates.
- State matrix and navigation spec templates.
- Accessibility and production review checklists.
- Mobile platform behavior notes.

Start with [docs/uiux/README.md](docs/uiux/README.md) for the documentation workflow.

## Publish checklist

Before publishing this repository to a skill directory or marketplace:

- Confirm every skill has a valid `.agents/skills/<name>/SKILL.md`.
- Keep each `SKILL.md` concise and agent-facing.
- Keep user/team documentation outside individual skill folders.
- Confirm each skill has `agents/openai.yaml` metadata.
- Avoid generated build artifacts, dependency folders, or private project files.
- Run `git status --short` and review all changed files before publishing.

