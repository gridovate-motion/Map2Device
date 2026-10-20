# Outdoor Map Converter v0.29 Public Beta RC1

**Bring your own raster maps to Garmin and TwoNav devices.**

**Developed by Gridovate Motion**

Outdoor Map Converter converts georeferenced raster maps automatically into the format required by the selected device:

- **Garmin** → KMZ / Garmin Custom Maps
- **TwoNav** → raster MBTiles

It can also read legacy **AMap/GeoGrid PDA maps (`.mph` + `.mpr`)** directly.

> **Public Beta RC1:** valid until **31 January 2027**. This prerelease is intended for compatibility testing on as many devices as possible.

## What can I use it for?

The tool is not limited to hiking maps. Any raster map that can be georeferenced reasonably well may be useful, for example:

- topographic and hiking maps
- **ski resort piste maps**, showing your own GPS position on the familiar resort map
- **city maps** for travel and sightseeing
- aerial imagery and orthophotos
- historical maps
- orienteering maps
- campus, event, park or site plans
- custom scale-accurate maps

A raster map does **not** become routable. Roads, lifts and attractions do not automatically become clickable POIs. The device can, however, show your current GPS position on top of the georeferenced map.

## Supported input

- GeoTIFF (`.tif`, `.tiff`) with embedded georeferencing
- AMap/GeoGrid PDA export (`.mph` + `.mpr`)

A plain JPG or PNG must currently be georeferenced first and exported as GeoTIFF. A built-in georeferencing assistant is planned for a later version but is **not included in this beta**.

## Installation on Windows

1. Download and extract the release ZIP.
2. Start `Outdoor_Map_Converter_v029_Public_Beta.exe`.
3. Choose **Deutsch** or **English** in the top-right corner.

No Python installation is required for this Windows build.

This Public Beta is currently **not code-signed**. Windows SmartScreen may therefore display a warning for a newly downloaded executable. Only run the file if it was downloaded from the official project release and, if desired, verify the SHA-256 checksum in `SHA256SUMS.txt`.

## How to use it

1. Select a GeoTIFF or the `.mph` file of an AMap/GeoGrid PDA map.
2. Check or edit the map name.
3. Select your **target device** from the alphabetical list.
4. Select quality. `Large area (Auto)` can be useful for very large Garmin maps.
5. Check the output path or choose your own with **Save as …**.
6. Click **Create Garmin KMZ** or **Create TwoNav MBTiles**.
7. Copy the finished map to your device.

A manually selected output folder always takes priority and will not be overwritten by automatic folder planning.

## Garmin

Garmin output is a Custom Map KMZ containing `doc.kml` and non-progressive JPEG tiles. The tile limit is set automatically from the selected device profile.

Typical target folder:

`Garmin\CustomMaps`

The Forerunner 970 has been tested on real hardware in this project. Other profiles are based on Garmin documentation or clearly marked practical sources.

## TwoNav

TwoNav output is raster MBTiles. Garmin tile limits do not apply.

Typical target folder:

`TwoNavData\Maps`

The generated MBTiles output has been **successfully tested in TwoNav Land on Windows**. Real-device tests on TwoNav hardware are welcome.

## No georeferenced map yet? Easy workflow with QGIS

QGIS is currently the easiest free option for city maps, piste maps, aerial images and scanned maps.

### Quick guide

1. Install QGIS.
2. Open **Raster → Georeferencer**.
3. Load your image or scan.
4. Add at least 3–4 clearly identifiable control points distributed across the map.
5. Assign the correct coordinates or pick the same points on the QGIS map.
6. In **Transformation settings**, choose a `.tif` output file.
7. Do not enable **Create world file only**.
8. Select a target CRS. Outdoor Map Converter will perform the required reprojection later.
9. Start georeferencing.
10. Open the resulting GeoTIFF in Outdoor Map Converter.

### Good control points

- city map: intersections, bridges, distinctive buildings
- ski map: base stations, mountain stations, peaks, distinctive lift junctions
- aerial image: road intersections, buildings, terrain features
- historical map: landmarks that can still be identified today

Control points should be spread across the full map. Highly distorted or illustrative tourist/piste maps may not georeference accurately over their entire extent.

## Hardware test feedback

For the Public Beta, tests on different Garmin and TwoNav models are especially valuable. Please report:

- manufacturer and model
- firmware version
- map detected: Yes/No
- position correct: Yes/No
- zoom complete: Yes/No
- white areas or rendering errors
- speed, crashes or other observations

See `HARDWARE_TEST_FEEDBACK.md`.

## Beta lifetime

This Public Beta is enabled until **31 January 2027**. After that date, a current build is required. The time limit is intended to keep outdated test versions from remaining in circulation indefinitely.

## Trademark and map-rights notice

Garmin and Garmin product names are trademarks of Garmin Ltd. or its subsidiaries. TwoNav and Land are trademarks or product names of their respective owners.

**Outdoor Map Converter is developed independently by Gridovate Motion and is not affiliated with, endorsed by, or tested by Garmin Ltd. or TwoNav/CompeGPS.** The trademarks are used solely to describe compatibility.

Users are responsible for ensuring they have the necessary rights to convert any maps, imagery, plans or other source material. The application does not include map content from Garmin, TwoNav, BEV or other map providers.

## Privacy

Map conversion is performed locally on the computer. This build does not require a user account and does not upload map data to Garmin, TwoNav or Gridovate Motion.

## Version

v0.29 Public Beta RC1, October 2026  
Developer / publisher: **Gridovate Motion**  
Copyright © 2026 Gridovate Motion. All rights reserved.
