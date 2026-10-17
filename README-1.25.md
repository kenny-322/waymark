# WAY●MARK 1.25 — Mobile foundation

This build starts the mobile-version work while preserving the existing travel-planning functionality.

## Added in 1.25
- Minimal animated startup screen while the first globe frame and Earth textures are loading.
- Early device-mode detection (`desktop` / `mobile`) using viewport and touch-pointer capabilities.
- Mobile top bar with a collapsible navigation menu and improved touch targets.
- Pointer-based globe dragging (mouse and touch) and two-finger pinch-to-zoom.
- Mobile-friendly safe-area handling for notches and full-screen dialogs.

## Preserved
- City catalog and city data files.
- Transport connections and route-building logic.
- Surprise route generator and saved journeys.
- Existing desktop layout and Earth texture URLs.

This is the first mobile foundation stage; route/cards and detailed mobile layouts still need testing and further refinement on real phones.
