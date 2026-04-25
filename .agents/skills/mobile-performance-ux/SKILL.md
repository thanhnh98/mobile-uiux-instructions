---
name: mobile-performance-ux
description: Improve perceived and actual mobile UX performance across loading, lists, images, pagination, animation, caching, and interaction responsiveness.
---

## When to use
- When building or reviewing feeds, lists, media-heavy screens, dashboards, search, maps, chat, or async feature flows.
- When users may experience slow network, large data sets, repeated refreshes, image loading, or expensive rendering.
- When UI feels correct but slow, jumpy, blocked, or battery-heavy.

## Core analysis model
- Separate actual performance from perceived performance.
- Define first useful paint, interactive readiness, refresh behavior, and completion feedback.
- Choose loading UI: skeleton, placeholder, progressive content, cached content, or blocking spinner.
- Review list rendering, pagination, virtualization, image loading, caching, prefetching, and memory pressure.
- Check animation cost, gesture latency, tap feedback, layout shifts, and avoidable re-renders.
- Plan offline, stale cache, retry, background refresh, and optimistic update behavior where relevant.

## Required outputs
- Performance risks.
- Perceived loading strategy.
- List and pagination strategy.
- Image/media loading strategy.
- Caching and refresh behavior.
- Responsiveness and animation notes.
- Measurement or test recommendations.

## References
- Read `references/performance-ux-reference.md` when a task needs a checklist for loading, lists, images, caching, refresh, animation, or release measurement.

## Anti-patterns to avoid
- Full-screen spinners when cached or partial content can be shown.
- Rendering large lists without virtualization or stable item keys.
- Loading full-resolution images into small thumbnails.
- Skeletons that do not match final layout and cause jumps.
- Blocking taps during non-critical background work.
- Animating layout-heavy properties on every frame.
- Refetching data on every screen focus without freshness rules.

## Implementation notes
- Use stable IDs, memoized rows, virtualization, pagination, and incremental rendering for long lists.
- Prefer thumbnails, responsive image sizes, lazy loading, placeholders, cancellation, and memory-aware caches.
- Keep skeleton dimensions close to final content to reduce layout shift.
- Show cached data immediately when it is safe; label or refresh stale data when user decisions depend on freshness.
- Debounce search and high-frequency inputs; make submit actions idempotent.
- Keep animations short, interruptible, and disabled or simplified under reduced motion.
- Measure with platform tooling or framework profilers when risk is high.

## Review questions
- What is the first useful thing the user sees?
- Does the screen remain responsive while data loads or refreshes?
- Can long lists scroll smoothly on low-end devices?
- Are images sized, cached, and cancelled correctly?
- Does pagination preserve scroll position and avoid duplicate items?
- Are loading, stale, offline, and retry states clear?
- What should be measured before release?
