# State Model Reference

## State Matrix Template

| State | Visible UI | Enabled Actions | Side Effects | Recovery Path |
| --- | --- | --- | --- | --- |
| Initial |  |  |  |  |
| Loading |  |  |  |  |
| Success |  |  |  |  |
| Empty |  |  |  |  |
| Partial |  |  |  |  |
| Error |  |  |  |  |
| Offline |  |  |  |  |
| Disabled |  |  |  |  |
| Submitting |  |  |  |  |
| Completed |  |  |  |  |
| Permission denied |  |  |  |  |
| Permission blocked |  |  |  |  |
| Session expired |  |  |  |  |
| Stale/deleted resource |  |  |  |  |

## Modeling Rules
- Model states as explicit variants where the framework supports it.
- Include visible UI, enabled actions, side effects, and recovery path per state.
- Prevent impossible state combinations.
- Keep state names user-meaningful and implementation-testable.
- Disable or debounce actions during submission and navigation transitions.
- Use cached or partial UI carefully; mark stale data when it affects decisions.

