# Chongqing Raffles City
[中文](README.md) · English

Advertising-grade Blender visualization of Chongqing Raffles City with 4K renders and a standalone realtime free-roam viewer.

Repository: [GitHub Repository](https://github.com/xiaojunxiong666-pixel/Chongqing-Raffles-City)

> This is an unofficial visual reconstruction and portfolio-style delivery. It is not BIM, a survey, an as-built record, an official digital twin, or an official representation of Raffles City, Chongqing, CapitaLand, or any other rights holder.

## Overview

This repository documents the v118 Chongqing Raffles City Blender visualization delivery. The public repository keeps documentation, third-party notices, release manifests, checksums, and promotional previews. The larger Blend parts, asset package, merge tools, and Viewer ZIP are published as GitHub Release v118 assets.

The geometry, materials, lighting, cameras, and scene come from the existing project delivery state. This publication uses an independent directory and does not write back to the original Blender project or rewrite the formal delivery ZIPs.

## Highlights

- Existing V2 architectural visual reconstruction for advertising stills and realtime presentation.
- Ten audited 3840×2160 PNG promotional renders with 1920×1080 JPEG previews in the repository.
- Package 05 provides a local realtime free-roam Viewer without Blender, Python, Node, or internet access.
- Packages 01, 02, and 04 merge into the final Blend on Windows; the merged result was reopened in Blender 5.2.1 LTS in background mode.
- All five formal ZIPs are below 100,000,000 bytes and have SHA-256 checksums.

## Project Scope

The factual boundary of this project is:

- The Chongqing Raffles City massing and urban context are visual reconstruction outputs.
- Public references and project pipeline data support visual identification; historical reference photos are not published as repository gallery or texture assets.
- Unmeasured building heights, distances, road widths, structural dimensions, and other engineering details are visual estimates, not surveyed facts.
- This project does not provide BIM, survey data, construction or as-built drawings, structural safety conclusions, official authorization, or digital-twin guarantees.

## Download

Open [GitHub Releases / v118](https://github.com/xiaojunxiong666-pixel/Chongqing-Raffles-City/releases/tag/v118). The five formal assets are:

| Canonical Chinese name | GitHub Release asset name | Purpose | Required |
| --- | --- | --- |
| 01_最终Blend_分卷1.zip | 01_FinalBlend_Part1.zip | Final Blend part 1 | Use with 02 and 04 |
| 02_最终Blend_分卷2.zip | 02_FinalBlend_Part2.zip | Final Blend part 2 | Use with 01 and 04 |
| 03_Assets素材_中文.zip | 03_Assets_CN.zip | Three Poly Haven CC0 HDRIs and asset notes | Optional; required images are packed in the final Blend |
| 04_合并工具与验证说明_中文.zip | 04_Merge_Verify_CN.zip | Windows merge scripts, instructions, and validation records | Required to merge 01 + 02 |
| 05_独立实时漫游Viewer_中文.zip | 05_Standalone_Viewer_CN.zip | Standalone local realtime Viewer | Use when you only need the Viewer |

GitHub automatically normalizes non-alphanumeric characters in Release asset names to ASCII. The left column is the formal source-package name and the right column is the actual GitHub download name; each asset label retains the formal Chinese name. SHA256SUMS.txt uses the actual download names.

The Git repository does not contain these five ZIPs, Blend files, GLB files, or HDR files. Keeping them as Release assets preserves the formal packages and their checksums while keeping the repository browsable.

## Full Blender Model

1. Download 01, 02, and 04.
2. Extract all three ZIPs into the same parent directory and preserve each package's top-level folder.
3. Open the 04_合并工具与验证说明 directory.
4. Double-click <code>MERGE_BLEND.cmd</code>. The Chinese launcher <code>合并并打开最终Blend.cmd</code> is also retained there.
5. The script recursively finds <code>.blend.part01</code> and <code>.blend.part02</code>, writes <code>重庆来福士_v118_最终模型.blend</code>, and normally attempts to open it with Blender.

The SHA-256 of the Blend actually produced during the clean extraction test was:

<code>f2e36b3a1e41138cfd841888353af8fdb269048c38f2c5df3a811f1c33213ccc</code>

The same test reopened the merged Blend with Blender 5.2.1 LTS in background mode and found no external linked libraries. Package 03 is still recommended if you want the separately delivered HDRI source files and their license records.

## Realtime Free-Roam Viewer

Download and fully extract 05_独立实时漫游Viewer_中文.zip, then double-click <code>打开实时漫游Viewer.cmd</code> in its root. It starts a loopback service and opens the default browser; if a port is occupied it tries subsequent ports.

The Viewer is a local offline package. Its service binds to 127.0.0.1 and does not require Blender, Python, Node, or internet access. Do not copy only the HTML file; keep the <code>viewer</code>, <code>exports</code>, <code>server</code>, and <code>vendor</code> directories together.

Closing the browser tab may leave the local PowerShell service running. The package has no dedicated Stop button; to stop it, end the matching <code>powershell.exe</code> in Task Manager whose command line contains <code>server\portable_server.ps1</code> and whose working directory is the extracted Viewer directory.

See the full [Viewer Guide](docs/VIEWER_GUIDE.md) for controls and troubleshooting.

## Controls

| State | Control |
| --- | --- |
| Default observation | Drag the mouse to orbit; use the wheel to zoom; select HERO, RIVER, CITY, CRYSTAL, PODIUM, LOW, HIGH, or PODIUM_CLOSE |
| Enter free roam | Click “进入自由漫游”; browsers with permission use pointer lock, otherwise hold the left mouse button to look |
| Movement | W forward, S backward, A left, D right |
| Elevation | Q down, E up |
| Boost | Shift |
| Speed | Select 6, 18, 45, or 100 m/s |
| Return to Hero | Home |
| Reset | “重置视角” restores the current preset |
| Exit free view | Esc exits pointer lock; click the button again to re-enter |
| Fullscreen | Use the “全屏” button or the browser's own fullscreen support |

## Tools & Workflow

- Blender 5.2.1 LTS; Cycles and EEVEE results in the project records are existing delivery evidence.
- The Viewer uses local three.js r186 runtime components, GLTFLoader, HDRLoader, and DRACOLoader.
- 01 and 02 are the split Blend required to respect the GitHub single-asset size limit; 04 only merges and validates them.
- Repository JPEGs are display previews generated from the existing 4K PNGs; the source PNGs were not rewritten by this publication.

## System Requirements

Full Blend:

- Windows, PowerShell, and Blender 5.2.1 LTS or a compatible newer version.
- Opening and rendering the complete scene needs substantial memory and GPU resources. Actual time depends on hardware, samples, resolution, and Blender settings; this project does not present one test machine as a minimum.

Realtime Viewer:

- 64-bit Windows 10/11 and a modern Chrome or Edge with WebGL2 support.
- 16 GB or more system memory and a discrete GPU are recommended; 32 GB and a stronger GPU are more comfortable for high-resolution displays or quality settings.
- Internet is not required after download; the browser must be allowed to reach local 127.0.0.1.

These Viewer recommendations are practical guidance, not a hard minimum measured across all hardware combinations.

## Data & Credits

Read [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) first.

- OpenStreetMap data is attributed to OpenStreetMap contributors under ODbL; the audited five release ZIPs contain no raw OSM snapshot.
- Copernicus WorldDEM-30 / GLO-30 provenance and adapted-data notice are retained according to the official requirements.
- The three HDRIs in package 03 are from Poly Haven and are recorded as CC0.
- The Viewer retains the relevant third-party notices for three.js and Draco runtime components.
- Historical reference photos are reference-only and are not redistributed in this repository or the five formal download packages.

## Disclaimer

This is an unofficial architectural visualization and realtime presentation. It does not represent official building documents, BIM or survey accuracy, engineering or safety findings, planning or property conclusions, brand authorization, or a digital-twin claim. Any building, road, urban-context, or scale detail without an explicit measured source should be treated as visual estimation.

Names and rights relating to the real building, companies, trademarks, maps, and data sources remain with their respective rights holders. This project does not imply collaboration, endorsement, or permission.

## License/Usage

This repository intentionally does not add a new LICENSE file and does not infer MIT, CC-BY, or commercial permission without explicit authorization. Original project content belongs to the project author. Third-party data, software, and assets remain under their original licenses. Obtain permission from the relevant rights holders and perform your own legal review before redistribution, commercial use, modification, or engineering use.

## Gallery

These are the 10 previews actually checked for this publication. They are 1920×1080 JPEGs generated from the existing 3840×2160 PNG renders for GitHub browsing.

| | |
| --- | --- |
| [![HERO RIVER CLOSE](docs/images/03_HERO_RIVER_CLOSE_v118_4K.jpg)](docs/images/03_HERO_RIVER_CLOSE_v118_4K.jpg) | [![CRYSTAL REVEAL](docs/images/04_CRYSTAL_REVEAL_v118_4K.jpg)](docs/images/04_CRYSTAL_REVEAL_v118_4K.jpg) |
| [![CITY SIDE WIDE](docs/images/05_CITY_SIDE_WIDE_v118_4K.jpg)](docs/images/05_CITY_SIDE_WIDE_v118_4K.jpg) | [![CITY SIDE HERO](docs/images/06_CITY_SIDE_HERO_v118_4K.jpg)](docs/images/06_CITY_SIDE_HERO_v118_4K.jpg) |
| [![LOW ANGLE SCALE](docs/images/07_LOW_ANGLE_SCALE_v118_4K.jpg)](docs/images/07_LOW_ANGLE_SCALE_v118_4K.jpg) | [![LOW CRANE HERO](docs/images/08_LOW_CRANE_HERO_v118_4K.jpg)](docs/images/08_LOW_CRANE_HERO_v118_4K.jpg) |
| [![CRYSTAL TERMINAL](docs/images/09_CRYSTAL_TERMINAL_v118_4K.jpg)](docs/images/09_CRYSTAL_TERMINAL_v118_4K.jpg) | [![CRYSTAL CENTER](docs/images/10_CRYSTAL_CENTER_v118_4K.jpg)](docs/images/10_CRYSTAL_CENTER_v118_4K.jpg) |
| [![PODIUM APPROACH](docs/images/11_PODIUM_APPROACH_v118_4K.jpg)](docs/images/11_PODIUM_APPROACH_v118_4K.jpg) | [![PODIUM CLOSE](docs/images/12_PODIUM_CLOSE_v118_4K.jpg)](docs/images/12_PODIUM_CLOSE_v118_4K.jpg) |
