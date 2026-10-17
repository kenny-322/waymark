# WAY●MARK 1.28 — Mobile rotation and search refinements

This build is based on 1.27. The new behavior is limited to the mobile UI mode (`data-device="mobile"`); desktop mouse behavior and desktop zoom range remain unchanged.

## Changes in 1.28
- Mobile swipe rotation increased by about 10% compared with 1.27.
- Mobile vertical rotation is limited to ±66°, preventing the globe from flipping upside down while allowing unrestricted horizontal rotation.
- Mobile pinch zoom-out limit increased from 7.6 to 8.5. The desktop zoom-out limit remains 7.6.
- Selecting a city in mobile search now animates yaw and pitch without a free quaternion rotation. The globe stays upright, removes roll, and preserves the same horizontal swipe direction after the transition.
- Mobile search still animates to the selected city at the medium zoom level (4.85). High-latitude cities stay as close to screen center as the no-flip vertical limit allows.
- A deliberate touch drag can interrupt the city-focus animation.

## Preserved
- 215-city catalog and city data.
- Transport connections, route-building logic, saved journeys, and surprise route generator.
- Earth textures, markers, labels, and the existing responsive layout.
- Desktop interaction settings.

## Validation
- JavaScript syntax check, archive integrity, and targeted static assertions were run for this build.
- A fully interactive browser/device test remains necessary to validate touch feel and city positioning in a browser that can load the Three.js CDN.
