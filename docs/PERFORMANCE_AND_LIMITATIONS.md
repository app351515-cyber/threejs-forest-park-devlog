# Saved performance records and caveats

The figures below are from **archived development/test reports**, not independently rerun measurements for this publication.

## Small forest — October 4, 2026

- Hardware: RTX 5060 Laptop GPU, 8 GB VRAM.
- 1080p, headless, DPR 1; one saved run after removing three trial effects from the normal configuration.
- Fixed view: **55.33 fps**
- Rotating view: **56.78 fps**

## Larger world — October 7, 2026

- Hardware: RTX 5060 Laptop GPU, 8 GB VRAM; other apps active.
- 1080p/high quality, approximately two ten-second runs for each view.
- Fixed view inside forest: **16.5 fps**
- Near waterfall: **21.3 fps**
- Rotating in forest: **16.3 fps**

**These are NOT matched A/B tests.** Scene sizes, viewpoints, and some settings differ. No saved result proves stable 60 fps throughout the 1 × 1 km world on this laptop.

## Other experiments

- An archived start-up-time experiment showed means changing from **77.12 s** to **42.96 s**. This is *not* a gameplay fps improvement; caching outside the application was not ruled out.
- Some leaf simplification tests lowered triangle counts but raised draw calls.
- A CPU-side cache experiment regressed against its baseline.

## Not claimed

- No comparable UE5 benchmark is available in this record.
- No claim that the whole 1 km world is 60 fps-ready.
- No independently audited GPU-frame-time methodology or complete telemetry.
