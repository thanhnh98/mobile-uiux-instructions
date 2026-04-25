---
name: mobile-production-review
description: Review mobile features and screens for production readiness across UX, state, navigation, accessibility, platform behavior, and code structure.
---

## When to use
- Before merging a mobile UI feature.
- When reviewing an existing feature for quality gaps or refactoring.
- When a screen feels visually acceptable but may fail real production use.

## Core analysis model
- Find missing states, weak hierarchy, CTA conflicts, fragile layout assumptions, accessibility gaps, platform inconsistencies, permission or notification gaps, navigation issues, and implementation smells.
- Prioritize issues by user impact and release risk.
- Separate must-fix items from polish.
- Tie design findings to concrete code or spec changes.
- Confirm adaptive behavior, dynamic text, offline/error recovery, and entry paths.

## Required outputs
- Issues by severity.
- What to fix first.
- Redesign direction.
- Implementation risks.
- Release-readiness checklist.

## References
- Read `references/production-review-reference.md` when a task needs a production review checklist, review prompt, accessibility checklist, platform notes, or severity framing.

## Anti-patterns to avoid
- Reviewing only visual style.
- Reporting preferences without user impact.
- Ignoring code structure and state ownership.
- Accepting missing denial, offline, or deep link behavior.
- Treating accessibility as a final-pass add-on.

## Implementation notes
- Use severity based on blocked task completion, data loss, broken navigation, inaccessible controls, or release regressions.
- Reference files, screens, states, and flows precisely.
- Recommend smallest changes that achieve production readiness.
- Include test gaps for state, navigation, accessibility, and permissions.

## Review questions
- What breaks outside the happy path?
- Can users recover from failure, denial, offline mode, or stale data?
- Does navigation behave correctly from every entry point?
- Are accessibility and dynamic text requirements met?
- Is the implementation maintainable enough to extend?
