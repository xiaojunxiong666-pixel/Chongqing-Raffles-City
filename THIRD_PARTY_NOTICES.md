# Third-Party Notices

This file records known third-party data, assets, and runtime components observed in the v118 delivery. It is an attribution record, not a grant of rights to the original project, building, trademarks, or unlisted content. Legal obligations can depend on the exact use and distribution; perform an independent review before redistribution or commercial use.

## OpenStreetMap

Project provenance records OpenStreetMap data obtained through a public Overpass API and local frozen snapshots. The OpenStreetMap license page states that the data is licensed under the Open Data Commons Open Database License (ODbL), requires credit to OpenStreetMap and its contributors, and requires making the ODbL availability clear.

Attribution:

OpenStreetMap contributors — data available under the Open Database License (ODbL): https://www.openstreetmap.org/copyright

The audited contents of the five formal v118 ZIPs contain no raw OSM snapshot file. Any future redistribution of raw or database-derived OSM data must independently satisfy ODbL obligations. The visual reconstruction is not an official OpenStreetMap product.

## Copernicus WorldDEM-30 / GLO-30

Project provenance records Copernicus DEM GLO-30, including the N29E106 tile, as a terrain source. The official Copernicus Data Space guidance provides the following notice for adapted or modified WorldDEM-30:

produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved

Source and licensing guidance:

- Copernicus DEM collection: https://dataspace.copernicus.eu/explore-data/data-collections/copernicus-contributing-missions/collections-description/COP-DEM
- Copernicus DEM GLO-30 license document: https://documentation.dataspace.copernicus.eu/APIs/SentinelHub/Data/DEM/resources/license/License-COPDEM-30.pdf

The five formal ZIP audits found no raw DEM tile file. This notice preserves the project provenance and required adapted-data attribution; it does not relicense Copernicus data.

## Poly Haven HDRIs

The project source manifest records the following HDRIs as CC0 1.0 assets from Poly Haven. Poly Haven's asset license states that its HDRIs, textures, and 3D models are released under CC0.

| Asset | Source page | Author record | SHA-256 |
| --- | --- | --- | --- |
| kloofendal_48d_partly_cloudy_puresky_4k.hdr | https://polyhaven.com/a/kloofendal_48d_partly_cloudy_puresky | Greg Zaal; Jarod Guest | 3061c00a16ecae748e84fd6c44c04804f539c118bb66325db858bad87b11bf88 |
| overcast_soil_puresky_4k.hdr | https://polyhaven.com/a/overcast_soil_puresky | Sergej Majboroda; Jarod Guest | 717958e9dfd092fcead82ff4691f3d615088803dd1888bb638ba948669021140 |
| qwantani_late_afternoon_puresky_4k.hdr | https://polyhaven.com/a/qwantani_late_afternoon_puresky | Greg Zaal; Jarod Guest | d820fa7a84732f69641655dcbea33b01ff78e6a4833ee3ca6f3bc938a0c09bb7 |

License: https://polyhaven.com/license

The three HDRIs are in 03_Assets素材_中文.zip. The Viewer package includes its local environment asset as part of the packaged runtime. Poly Haven branding and website content are not being claimed as project content.

## three.js

The Viewer bundles three.js r186 modules and utilities, including the local three.js core module and loader utilities. The package includes <code>viewer\vendor\THREE_LICENSE</code>.

License: MIT
Copyright: 2010-2026 three.js authors
Official source: https://github.com/mrdoob/three.js/blob/dev/LICENSE
The local Viewer uses GLTFLoader, HDRLoader, DRACOLoader, BufferGeometryUtils, and SkeletonUtils in addition to three.js core modules. They remain third-party components under their applicable upstream license.

## Draco

The Viewer includes the Draco glTF decoder runtime under <code>viewer\vendor\draco\gltf</code>. The upstream Google Draco repository identifies the project as Apache-2.0 and its LICENSE file is available here:

https://github.com/google/draco/blob/main/LICENSE

This notice records the bundled decoder as an Apache License 2.0 component. The Apache license terms, including retention of applicable notices and inclusion of the license when redistributing the component, continue to apply to that component.

## Project Outputs and Reference Material

- The Blender scene, project scripts, final renders, and Viewer integration are project outputs. No new open-source license is granted for them by this repository.
- Historical reference photographs used during modeling are reference-only and are not included in the repository gallery or the five formal v118 ZIPs.
- No separate font file or third-party PBR texture pack was found in the audited publication inputs.
- Names, logos, building designs, and trademarks connected with the real-world site remain subject to the rights of their respective owners. This project does not imply affiliation or endorsement.
