<p align="center"><img src="docs/assets/mark.svg" width="56" alt="Simple Diffusion"></p>
<h1 align="center">Simple Diffusion</h1>
<p align="center"><b>Pick a style. Describe it. Create.</b><br>Free local AI image generation for Windows, by Prosper Technologies.</p>
<p align="center"><a href="https://prospertechnology.github.io/simple-diffusion/">Product website</a> · <a href="https://github.com/ProsperTechnology/simple-diffusion/releases/tag/v0.5.1">Download v0.5.1</a> · <a href="https://prospertechnology.github.io/simple-diffusion/guide.html">Installation guide</a> · <a href="CHANGELOG.md">Release history</a></p>

![Simple Diffusion 0.5 Windows studio showing an image generated locally on an NVIDIA GPU](docs/assets/studio.jpg)

Simple Diffusion is a Windows desktop app for creating SDXL images on your own NVIDIA graphics card. Basic local generation is free: no account, no image credits and no telemetry. Download the model once, then generate offline.

**Current status:** v0.5.1 is an **unsigned early-access prerelease**. Verified on Windows 11 with RTX 4080 / 16 GB. Broader hardware testing remains pending. Automatic updates and live pack sales are disabled.

## Download and install

Open the [official v0.5.1 release](https://github.com/ProsperTechnology/simple-diffusion/releases/tag/v0.5.1) and download **all three files**:

1. `Simple-Diffusion-Setup-0.5.1.exe`
2. `Simple-Diffusion-Setup-0.5.1-1.bin`
3. `Simple-Diffusion-Setup-0.5.1-2.bin`

Keep them in the same folder, then open the setup executable. The installer includes its own Python/NVIDIA engine; separate developer tools or CUDA installation are not required. The model downloads separately during setup (~6.9 GB). The release includes `SHA256SUMS.txt` for integrity checks; a matching hash is not a publisher signature.

The build is unsigned and Windows may show an unrecognized-publisher warning. If you prefer signed software, wait for a signed release. See the [complete installation guide](https://prospertechnology.github.io/simple-diffusion/guide.html).

## In the studio

| Feature | What you can do |
|---|---|
| Local SDXL generation | Create square, portrait or landscape images on supported NVIDIA hardware |
| Curated styles | Start with Photography, Illustration or Stylized 3D |
| Guided editing | Make reference-image variations or paint an area to change |
| Projects and gallery | Save a project, search prompts/style names and reuse image settings |
| Export | Save PNG/JPEG originals or destination-sized, cropped exports |
| Personal workspace | Choose Midnight/Paper, focus the canvas and find actions with Ctrl+K |
| Draft recovery | Recover the last prompt/name/settings locally; saved projects restore reference/edit context |
| Recipe packs | Install validated data-only packs with real per-style previews |

## Release protection in 0.5.1

The release omits readable first-party Python source, source maps and private development files. Desktop code is compacted; production debugging hooks are disabled. The app verifies its archive and worker integrity. Packaging checks enforce these settings and reject QA launchers.

These measures deter casual copying and tampering. Offline desktop software can still be reverse engineered; this is not source encryption or an absolute protection guarantee. Third-party components retain their licenses. The older 0.5.0 installer is superseded.

## Studio improvements

- Midnight and Paper appearances, remembered locally.
- Searchable Ctrl+K actions, arrow-key navigation, focus management and canvas focus mode.
- Last prompt/settings recovery and gallery search by style name.
- Fixed overlapping jobs during model verification, preparation cancellation, stale mask callbacks and immediate worker-event races.
- Updated Electron, React and build/test dependencies.

[Full changelog](CHANGELOG.md) · [Detailed release notes](https://prospertechnology.github.io/simple-diffusion/releases.html)

## Requirements

| Component | Requirement |
|---|---|
| System | Windows 10/11 x64 target; currently tested on Windows 11 |
| Graphics | NVIDIA GPU with **8 GB+ VRAM**, driver **560.94+** |
| System memory | **16 GB RAM** or more |
| Storage | Allow **20 GB+ free** for setup/extraction/model; images need more space |
| Network | Required for downloads; generation runs offline after setup |

Test machine: RTX 4080 / 16 GB VRAM. Physical 8/12 GB GPUs and fresh Windows installations still need testing. AMD, Intel, CPU-only, Linux and macOS generation are unsupported in this release. No head-to-head Fooocus quality, speed or memory superiority has been established.

## Five collections, thirteen style recipes

| Collection | Styles | Availability |
|---|---|---|
| The Starter Collection | Photography, Illustration, Stylized 3D | Included free |
| Warm Light | Warm Editorial | Free optional pack |
| Studio Light | Softbox Studio, Direct Flash, Low Key | $5 one-time **TEST** checkout; live sales disabled |
| Object Studies | Soft Neutral, Color Block, Glass & Glow | $5 one-time **TEST** checkout; live sales disabled |
| Paper Worlds | Layered Paper, Linocut Print, Folded Worlds | $5 one-time **TEST** checkout; live sales disabled |

Packs are style recipes, not additional models. Examples are generated locally; results vary with prompt and seed. [Explore the collections](https://prospertechnology.github.io/simple-diffusion/#collections).

## Privacy and updates

Images, prompts, projects, references and draft recovery stay in the local Windows profile. No inference API or telemetry is used. Setup downloads the pinned model files. Opening GitHub or an optional test checkout opens an external service with its own privacy policy. [Privacy and licenses](https://prospertechnology.github.io/simple-diffusion/privacy.html).

The updater foundation verifies signed manifests and Windows-signed installers. **Live automatic updates are disabled** until release signing is configured. Manual prerelease downloads are available above.

## Help and bug reports

Use Settings → Help & diagnostics to copy a sanitized report. For missing/damaged model files, use Set up / repair. Report reproducible issues in the [official tracker](https://github.com/ProsperTechnology/simple-diffusion/issues), including app version, Windows version, GPU/VRAM, steps and expected/actual behavior. Never post private prompts, images, account details or personal folder paths.

## Repository and licenses

This is Prosper Technologies’ official **product-information and distribution repository**. Application source is privately maintained; this repository does not grant an open-source application license. Third-party components retain their licenses. The SDXL model uses the [CreativeML Open RAIL++-M license](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/blob/main/LICENSE.md), reviewed during setup. Simple Diffusion is independently implemented and contains no Fooocus application source.

Public data: [product.json](product.json) · [Changelog](CHANGELOG.md) · [Website sitemap](https://prospertechnology.github.io/simple-diffusion/sitemap.xml)
