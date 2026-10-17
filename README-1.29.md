# WAY●MARK 1.29 — Mobile swipe feel refinement

This build is based on WAY●MARK 1.28. The new swipe movement is limited to single-finger touch dragging when the mobile UI is active. Desktop mouse behavior and all other desktop settings are preserved.

## Changes in 1.29
- Mobile globe rotation now maps touch distance directly to angular movement, avoiding the old frame-time-dependent velocity calculation.
- Horizontal sensitivity is 0.005 radians per CSS pixel: a 300px drag corresponds to about 86° of globe rotation before the small release glide.
- Vertical sensitivity is 0.0042 radians per CSS pixel and continues to respect the existing ±66° anti-flip limit.
- Release inertia is modest and capped (4.2 rad/s horizontal, 2.4 rad/s vertical before a 0.62 release factor), so quick swipes feel responsive without allowing an uncontrolled spin.
- The existing city-search focus, medium zoom, pinch-to-zoom, expanded mobile zoom-out limit, and free horizontal rotation are preserved.

## Preserved
- 215-city catalog and city data.
- Transport routes, saved journeys, surprise route generator, Earth textures, markers, and labels.
- Desktop mouse rotation, automatic edge rotation, and desktop zoom range.

## Validation
- JavaScript syntax and ZIP integrity should be checked before publishing.
- Real touch feel should still be confirmed on the target phone/browser; browser/device testing depends on the external Three.js CDN loading successfully.
