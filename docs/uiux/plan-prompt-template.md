# Plan Prompt Template

Use this prompt with Codex before building a mobile feature.

```text
Use the mobile-feature-planning, mobile-state-model, mobile-navigation-stack, mobile-permission-notification, mobile-accessibility, mobile-adaptive-layout, mobile-performance-ux, and mobile-engineering-handoff skills.

Plan this mobile feature for production implementation:

Feature:
[describe the feature]

Target platform/framework:
[iOS / Android / React Native / Flutter / Kotlin Multiplatform / other]

Known requirements:
[list requirements]

Constraints:
[API, design system, navigation, auth, analytics, deadlines]

Produce:
- Feature intent
- Flow summary
- Key screens
- State matrix
- Navigation model
- Permission/notification considerations
- Accessibility and adaptive layout risks
- Performance UX risks
- Proposed file/component structure
- Implementation warnings

Keep the plan concise and implementation-ready. Do not write code yet unless explicitly asked.
```
