# Engineering Handoff Reference

## Build Prompt Template

```text
Use the mobile-screen-uiux, mobile-layout-structure, mobile-state-model, mobile-navigation-stack, mobile-accessibility, mobile-adaptive-layout, mobile-performance-ux, and mobile-engineering-handoff skills.

Implement this mobile feature:

Feature/spec:
[paste or link the approved plan/spec]

Target files or area:
[paths, modules, screens, routes]

Design/source references:
[Figma, screenshots, existing components, design system notes]

Implementation rules:
- Keep screen files thin.
- Split reusable UI into focused components.
- Include loading, empty, error, offline, disabled, submitting, and blocked states where relevant.
- Respect platform-native navigation, permissions, keyboard, safe area, and accessibility behavior.
- Add semantic labels for interactive elements.
- Keep loading, lists, images, pagination, refresh, and animations responsive.
- Add or update focused tests where risk justifies it.

After implementation, summarize changed files, state coverage, accessibility handling, performance UX handling, and any remaining risks.
```

## Handoff Checklist
- Suggested files:
- Screen shell:
- Section components:
- Reusable primitives:
- State renderers:
- Feature-specific components:
- State owner:
- Navigation effects:
- Analytics events:
- Platform differences:
- Test focus:

