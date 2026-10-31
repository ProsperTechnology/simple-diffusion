# Release history

## 0.6.0 — 2026-10-31 · optional engine download

- App-only Windows installer: 169 MB. The large NVIDIA engine is no longer bundled or fetched by Windows setup.
- First-run setup shows engine/model download sizes and can be dismissed until the user is ready.
- Explicit setup downloads the verified NVIDIA engine and SDXL model with pause/resume. Failed downloads or extraction cannot become a ready engine.
- Versioned engines stay in local app data across normal app updates. Existing model files are verified and reused.
- Verified: 27 automated tests, app-only installation, clean first run without an engine, separate engine extraction, and packaged real GPU generation, export and cancellation.
- Still unsigned early access. Automatic updates and live sales remain disabled.

## 0.5.1 — 2026-10-30 · release hardening

- Release builds now compact the first-party desktop JavaScript and omit source maps and development files.
- The first-party Python worker ships as interpreter-matched bytecode, with a hash checked at application startup. Readable worker.py is absent from the release.
- Enabled Electron archive integrity validation and ASAR-only loading; disabled Node-mode, Node options injection, Node inspector flags and packaged renderer developer tools.
- Added a fail-closed packaging check for private source/build artifacts, worker integrity and required fuse settings. QA/debug launchers cannot enter the installer.
- Added Prosper Technologies copyright notice while preserving third-party notices and licenses.

Verification: 22 automated test groups pass; compacted app and bytecode worker passed actual GPU generation, JPEG export and cancellation; all five collections/13 styles passed import, previews and restart tests. A separate QA executable enabled only its inspector for automation and was removed before packaging. The sealed production executable launched normally, and a modified ASAR was rejected by its integrity check.

These measures deter casual copying and tampering. JavaScript compaction and Python bytecode are not encryption; determined users can still inspect or reverse engineer software running on their PC. Locally installed recipe packs and public model weights remain accessible. No server secrets are bundled. Previously downloaded versions cannot be recalled. The older 0.5.0 installer was withdrawn from public downloads after 0.5.1 was verified.

This release remains unsigned; code signing and broader hardware/security review are pending. Automatic updates and live sales remain disabled. October 31 packaging update: a single-download online setup now fetches and verifies installation data automatically. Internet is required during installation.

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
