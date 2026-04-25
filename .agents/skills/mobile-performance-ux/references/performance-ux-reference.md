# Performance UX Reference

## Loading Strategy
- Prefer cached or partial content over blocking full-screen spinners when safe.
- Match skeleton dimensions to final content to avoid layout jumps.
- Define first useful paint, interactive readiness, refresh behavior, and completion feedback.

## Lists and Pagination
- Use stable IDs, memoized rows, virtualization, pagination, and incremental rendering for long lists.
- Preserve scroll position during pagination and refresh.
- Avoid duplicate items when merging pages or handling retries.

## Images and Media
- Load thumbnails or responsive sizes for small containers.
- Cancel off-screen image work where the framework supports it.
- Use placeholders and caching to reduce perceived wait.
- Account for memory pressure on low-end devices.

## Caching and Refresh
- Show cached data immediately when it is safe.
- Label or refresh stale data when user decisions depend on freshness.
- Debounce search and high-frequency inputs.
- Make submit and retry actions idempotent.

## Animation and Responsiveness
- Keep animations short, interruptible, and reduced under reduced motion.
- Avoid animating layout-heavy properties on every frame.
- Keep tap feedback immediate even when background work continues.

## Measurement
- Profile screens with large lists, media, maps, chat, dashboards, or search.
- Check low-end device behavior, slow network, pagination, refresh, and image-heavy paths before release.

