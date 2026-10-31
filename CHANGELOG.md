# Release history

## 0.5.0 — 2026-10-30 · early-access prerelease

- New Midnight appearance with a matching dark composer, library, store and dialogs; Paper appearance remains available. Appearance is remembered locally.
- Ctrl+K quick actions with search, arrow-key navigation and keyboard focus management.
- Canvas focus mode; Escape restores the composer.
- Local recovery of the last prompt, project name and generation settings after restart. Saved projects remain the way to restore reference images and painted selections.
- Gallery search now matches style names as well as prompts.
- Fixed overlapping generation requests during model verification; preparation reports busy and blocks engine restart, folder changes and update installation. Cancellation prevents the prepared job from starting.
- Fixed stale mask-loading callbacks and cleared reference/mask state when choosing a new-image example.
- Fixed an immediate worker completion/error race and duplicate Create submissions in the interface.
- Updated Electron to 45.2.1, React to 19.3.1, Vite to 7.3.7, electron-builder to 26.18.0 and Playwright to 1.64.1. Removed the unused npm build dependency.
- Rebuilt product documentation, download instructions, public website and repository presentation.

Verification: 20 automated test groups; real local GPU generation, JPEG export, cancellation and painted-area generation; preparation concurrency/cancellation checks; theme, keyboard, focus, draft recovery and compact-window checks; five-collection installation/preview/restart checks. Tested on Windows 11 with an RTX 4080 (16 GB). Broader hardware testing remains pending.

This is an **unsigned Windows testing build**. Automatic update installation is disabled until release signing is configured. Paid collections use **test checkout only**; live purchasing is disabled. One moderate advisory remains in a transitive build-only minimatch dependency; it is not bundled in the desktop application's production dependencies. No independent security audit is claimed.

## 0.4.0 · development milestone

Completed the five-collection catalog, 13 style recipes, real per-style preview selectors, three $5 one-time test checkout pages, and downloadable pack kits. Two collections are included/free. Live sales remained disabled.

## 0.3.2 · development milestone

Added embedded PNG pack previews, artwork compatibility for earlier installed packs, private previews after first generation, preview refresh on re-import, and stricter image validation.

## 0.3.0 · development milestone

Added the in-app pack storefront and signed-manifest updater foundation. Automatic checks and installation remained disabled pending release signing.

## 0.2.0 · development milestone

Introduced the redesigned studio, local gallery, projects, reference variations, painted-area corrections, destination-sized exports, setup/repair screens, and Inno Setup installer with bundled NVIDIA runtime.

## 0.1.0 · development milestone

Established local SDXL generation, three starter styles, verified model setup and a dedicated offline Python worker.

Earlier entries describe internal development milestones, not historical public GitHub releases. The 0.5.0 prerelease is the first published installer in this repository.
