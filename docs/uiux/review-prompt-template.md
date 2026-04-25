# Review Prompt Template

Use this prompt to review or refactor an existing mobile feature.

```text
Use the mobile-production-review, mobile-state-model, mobile-navigation-stack, mobile-permission-notification, mobile-accessibility, mobile-adaptive-layout, mobile-performance-ux, and mobile-engineering-handoff skills.

Review this mobile feature for production readiness:

Feature/screen:
[name and purpose]

Relevant files:
[paths]

Known concerns:
[bugs, UX issues, design drift, accessibility, state, navigation, platform behavior]

Review for:
- Missing or weak states
- Poor hierarchy or CTA conflicts
- Navigation and back behavior issues
- Deep link or notification entry risks
- Permission denial and settings recovery gaps
- Accessibility and dynamic text gaps
- Adaptive layout failures
- Performance UX issues in loading, lists, images, pagination, caching, or animation
- Implementation smells and test gaps

Return issues by severity with file references where possible, what to fix first, redesign direction, and release-readiness status.
```
