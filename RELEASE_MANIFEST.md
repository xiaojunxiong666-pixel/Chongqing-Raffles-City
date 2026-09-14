# Release Manifest — v118

## Publication scope

- Repository display name: Chongqing Raffles City
- Repository slug: Chongqing-Raffles-City
- Repository URL: https://github.com/xiaojunxiong666-pixel/Chongqing-Raffles-City
- Intended visibility: public
- Intended default branch: main
- Release tag: v118
- Release title: Chongqing Raffles City — v118
- Publication directory: D:\Blender\CHONGQING_CITY_V1\delivery\GITHUB_PUBLISH\Chongqing-Raffles-City
- Source project root: D:\Blender\CHONGQING_CITY_V1
- Original project modification: no
- Formal source ZIP modification: no
- Repository policy: documentation, manifests, checksums, notices, and preview JPEGs only; large delivery packages stay as Release assets

## Formal Release assets

All five source ZIPs were read from D:\Blender\CHONGQING_CITY_V1\delivery\FINAL_PACKAGES. The byte counts and SHA-256 values below match the project delivery state and the pre-publication audit.

| Release asset | Bytes | SHA-256 | Content |
| --- | ---: | --- | --- |
| 01_最终Blend_分卷1.zip | 88587274 | 4ec86c0ecca80a7f6cdec56ee21d770e293d18304d1e5e90ef73e80e04dd5542 | Blend part 01 and split note |
| 02_最终Blend_分卷2.zip | 68141921 | 0ab91901a4e6fe6d163ee218796479a78fb815377f89db91363fa9d08971bfbd | Blend part 02 and split note |
| 03_Assets素材_中文.zip | 34137504 | d95c3022e20b44836c62bdb8e9ef3c1320304466a354b17ae5de7ae87fa353d5 | Three HDRIs and asset note |
| 04_合并工具与验证说明_中文.zip | 4806 | a6d73f084cf584a307eb8ed8b9b3082b956881d3db1bd9c312327e93fa73c7f9 | Merge tools, instructions, and QA records |
| 05_独立实时漫游Viewer_中文.zip | 40577418 | a936924b434d56f1fccf7ee0ebccecafccb6792d40e794f43677b8f354854487 | Offline local Viewer and packaged GLB |

The formal Release also includes SHA256SUMS.txt. Historical duplicate folders and ZIPs in FINAL_PACKAGES are deliberately excluded.

## Package entry summary

01 contains:

- 01_最终Blend_分卷1\重庆来福士_v118_最终模型.blend.part01
- 01_最终Blend_分卷1\分卷说明.txt

02 contains:

- 02_最终Blend_分卷2\重庆来福士_v118_最终模型.blend.part02
- 02_最终Blend_分卷2\分卷说明.txt

03 contains:

- 03_Assets素材\素材说明.txt
- 03_Assets素材\HDRI\kloofendal_48d_partly_cloudy_puresky_4k.hdr
- 03_Assets素材\HDRI\overcast_soil_puresky_4k.hdr
- 03_Assets素材\HDRI\qwantani_late_afternoon_puresky_4k.hdr

04 contains:

- 合并并打开最终Blend.cmd
- 合并最终Blend.ps1
- 中文使用说明.txt
- Blend新电脑重开验证.json
- MERGE_BLEND.cmd
- merge_blend.ps1
- Viewer浏览器验证.json

05 contains these entries:

- 00_中文入口_先看.txt
- 04_DOCS\B03_REMOVE_ALL_B02_CONTEXT_AUDIT_V118.json
- 04_DOCS\B05_REALTIME_VIEWER_BROWSER_QA.json
- 04_DOCS\GLB_STRUCTURE_QA.json
- 04_DOCS\PACKAGE_MANIFEST.json
- 打开实时漫游Viewer.cmd
- 启动本地Viewer.ps1
- 使用说明_先看.txt
- 中文说明_先看这里.txt
- CHECKSUMS.sha256
- exports\
- exports\viewer\latest.json
- exports\viewer\v118r3\重庆来福士_v118_Viewer模型.glb
- exports\viewer\v118r3\GLB_STRUCTURE_QA.json
- exports\viewer\v118r3\manifest.json
- launch_viewer.ps1
- runtime\module-test.html
- runtime\module-test2.html
- runtime\module-test2.mjs
- runtime\viewer-server.stderr.log
- runtime\viewer-server.stdout.log
- runtime\viewer-service.json
- server\portable_server.ps1
- viewer\assets\kloofendal_48d_partly_cloudy_puresky_4k.hdr
- viewer\index.html
- viewer\published-model.mjs
- viewer\vendor\draco\
- viewer\vendor\draco\gltf\draco_decoder.js
- viewer\vendor\draco\gltf\draco_decoder.wasm
- viewer\vendor\draco\gltf\draco_wasm_wrapper.js
- viewer\vendor\DRACOLoader.js
- viewer\vendor\GLTFLoader.js
- viewer\vendor\HDRLoader.js
- viewer\vendor\THREE_LICENSE
- viewer\vendor\three.core.js
- viewer\vendor\three.module.js
- viewer\vendor\utils\BufferGeometryUtils.js
- viewer\vendor\utils\SkeletonUtils.js

The full path-level audit, including byte sizes, remains in the local publication logs.

## Verification evidence

- ZIP audit: five exact source ZIPs opened with .NET ZipFile; no duplicate entries, unsafe paths, read errors, or sensitive filenames.
- Size gate: all five ZIPs are below 100,000,000 bytes.
- Merge audit: a common extraction of 01, 02, and 04 produced the actual file 重庆来福士_v118_最终模型.blend with SHA-256 f2e36b3a1e41138cfd841888353af8fdb269048c38f2c5df3a811f1c33213ccc.
- Blender reopen: Blender 5.2.1 LTS background reopen passed; 9840 objects, 3608 meshes, 106 materials, 4 images, 0 linked libraries, 1 scene.
- Viewer launch: a clean extraction of 05 started its portable service on 127.0.0.1, returned HTTP 200 for /status and /viewer/, and opened in Microsoft Edge.
- Viewer QA reuse: the package's B05_REALTIME_VIEWER_BROWSER_QA.json reports model readiness, HDRI readiness, zero console errors, eight presets, WASD/QE/Shift/Home behavior, and pointer-lock fallback. A fresh CUA interaction was unavailable because the computer-use backend returned nodeRepl.fetch request failed; no new mouse/keyboard result is claimed.
- Promo image audit: 10 source PNGs were readable, unique by SHA-256, and 3840×2160; 10 independent 1920×1080 JPEG previews were generated without changing sources.
- Path audit: diagnostic JSON files preserve original project provenance paths; no user profile, credential, or secret filename was found in the five package entry names. These preserved project paths are called out rather than silently rewritten.
- License audit: PASS for recorded sources; see THIRD_PARTY_NOTICES.md.

## Repository contents

The Git repository contains:

- README.md and README_EN.md
- RELEASE_MANIFEST.md
- SHA256SUMS.txt
- THIRD_PARTY_NOTICES.md
- docs/VIEWER_GUIDE.md
- docs/RELEASE_NOTES_v118.md
- docs/images/*.jpg (10 preview images)

The Git repository excludes ZIP, Blend, GLB, HDR, WASM and local log files through the publication policy. Exact Release assets are verified separately on the v118 Release page.
