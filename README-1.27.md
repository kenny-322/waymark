# WAY●MARK 1.27 — Mobile interaction fixes

This build refines mobile interaction based on feedback while preserving the 1.26 project structure and travel-planning features.

## Added in 1.27
- Mobile touch-swipe speed increased by a further 15% over the 1.26 mobile setting (about 1.403× the original drag velocity); desktop mouse movement is unchanged.
- Mobile vertical rotation no longer clamps at the top or bottom, allowing full free rotation in every direction.
- Mobile edge-hover/edge-touch auto-rotation is disabled; the globe moves only from deliberate drag gestures or other explicit controls.
- Fixed mobile search-focus animation so the render loop cannot overwrite its rotation; selecting a search result now smoothly brings the chosen city toward the camera and ends at the medium zoom (4.85).
- The farther zoom-out limit from 1.26 is preserved.

## Preserved
- City catalog and city data files.
- Transport connections, route-building logic and saved journeys.
- Surprise route generator and existing desktop/mobile layouts.
- Earth textures, city markers and labels.

## Testing note
- JavaScript syntax and ZIP integrity were checked.
- A live browser/device interaction test could not be completed in this environment; verify touch feel and the search transition after uploading the build to a browser with access to the Three.js CDN.
