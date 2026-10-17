# WAY●MARK 1.30 — Zoom-adaptive mobile swipe sensitivity

This build is based on WAY●MARK 1.29. It adjusts swipe sensitivity only in the mobile touch-drag path; desktop mouse/touch behavior is unchanged.

## Changes in 1.30
- Globe rotation sensitivity decreases smoothly as the camera zooms in, making close-up city browsing more precise.
- A smoothstep curve avoids abrupt jumps between zoom levels.
- At the minimum mobile camera distance (3.25), rotation sensitivity is 55% of the existing 1.29 value.
- At the maximum mobile zoom-out distance (8.5), sensitivity remains at 100%, preserving the fast swipe feel when zoomed out.
- Intermediate zoom levels interpolate smoothly between those values. Both horizontal and vertical swipe rotations use the same zoom-dependent factor; release glide uses the scaled rotation velocity too.

## Preserved
- Desktop interaction and desktop zoom limits.
- Mobile city search focus, medium search zoom, pinch zoom, pitch limit, and free horizontal rotation.
- 215-city catalog, transport routes, saved journeys, surprise route generator, Earth textures, markers, and labels.

## Validation
- JavaScript syntax check passed with Node.js.
- ZIP integrity and required project files checked.
- Touch feel should be confirmed on the target phone/browser after publishing; no physical device test was available here.
