<!-- Copyright (c) Manfred Foissner. All rights reserved. License: See LICENSE.txt -->

# BONZOOKAA v2 - Changelog

## v2.0.0 p001 — Exploration Stabilize
**ZIP:** `BONZOOKAA_v2.0.0_p001_ExplorationStabilize.zip`

### Changed
- Zones now include `bounds` metadata (`{ minX, minY, maxX, maxY }`) to support consistent world-space simulation.

### Fixed
- MapGenerator: fixed obstacle density initialization (cfg-driven).
- MapGenerator: elite spawn density now uses the computed depth/mod scaled value.
- Bullets: offscreen culling now uses zone/world bounds while exploring.
- Enemies: exploration-spawned enemies are not killed by canvas bounds; shooting gating uses player distance.
- Pickups: floor bounce now uses zone height while exploring.

## v2.0.0 p002 — Remove Legacy Start Modal
**ZIP:** `BONZOOKAA_v2.0.0_p002_RemoveLegacyStartModal.zip`

### Removed
- Removed the legacy "START RUN" modal (`#startModal`) from `index.html`.

### Fixed
- Eliminated a crash path caused by the legacy modal invoking a non-existent `Game.start()` handler.

### Changed
- Hub is now the sole entry point for starting runs (via Act selection).
