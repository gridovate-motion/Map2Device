# Map2Device

**Raster maps optimized for watches & outdoor GPS devices.**

**by Gridovate Motion**

[![Download for Windows](https://img.shields.io/badge/Download_for_Windows-v0.30_Public_Beta-0B5ED7?style=for-the-badge&logo=windows)](https://github.com/gridovate-motion/Map2Device/releases/download/v0.30-public-beta/Map2Device_v030_Public_Beta.exe)

**Windows 10/11 · 64-bit · Portable · No installation required**

> **Public Beta:** valid until **31 January 2027**. Map2Device is currently unsigned, so Windows SmartScreen may display an “Unknown publisher” warning. Download it only from the official Gridovate Motion GitHub release.

[Release page and checksum](https://github.com/gridovate-motion/Map2Device/releases/tag/v0.30-public-beta) · **Deutsch:** [README_DE.md](README_DE.md)

---

## What is Map2Device?

Map2Device prepares georeferenced raster maps for compatible **Garmin** and **TwoNav** devices. It does more than change a file extension: it creates a device-ready map structure and applies the appropriate tiling, resolution, file-size and device-limit logic for the selected target.

**Map → Device**

Current output:
- **Garmin** → KMZ / Garmin Custom Maps
- **TwoNav** → raster MBTiles

Supported input:
- GeoTIFF (`.tif`, `.tiff`) with embedded georeferencing
- legacy AMap / GeoGrid PDA maps (`.mph` + `.mpr`)

## Typical use cases

Map2Device can be used with many kinds of georeferenced raster maps, for example:
- orienteering maps
- hiking and topographic maps
- ski resort piste maps
- city and tourist maps
- aerial imagery and orthophotos
- historical maps
- campus, park, event or site plans

The result is still a raster map. Roads, lifts and POIs do not automatically become routable or interactive, but the device can display the user's GPS position on the georeferenced map.

## Quick start

1. Download `Map2Device_v030_Public_Beta.exe`.
2. Start the EXE. No installation is required.
3. Select a GeoTIFF or the `.mph` file of an AMap/GeoGrid PDA map.
4. Select the target device or use **Manual / other device**.
5. Choose quality and output location.
6. Create the Garmin KMZ or TwoNav MBTiles file.
7. Copy the result to the device.

A manually selected output folder always has priority.

## Garmin

Garmin output is a Custom Map KMZ with `doc.kml` and non-progressive JPEG tiles. Device-specific tile limits are applied automatically from the selected profile.

Typical destination:

`Garmin\CustomMaps`

The **Forerunner 970** has been tested on real hardware in this project. Other profiles are based on manufacturer documentation or clearly marked practical sources. A manual profile allows testing additional devices.

## TwoNav

TwoNav output is raster MBTiles. Garmin tile limits do not apply.

Typical destination:

`TwoNavData\Maps`

The generated MBTiles output has been successfully tested in **TwoNav Land on Windows**. Real-device feedback is welcome.

## No georeferenced map yet?

For JPG/PNG scans, city maps, ski maps or other images without georeferencing, **QGIS** is currently the recommended free workflow.

### Simple QGIS workflow
1. Open **Raster → Georeferencer**.
2. Load the image or scan.
3. Add at least 3–4 well-distributed control points.
4. Assign the corresponding real-world coordinates.
5. Choose GeoTIFF (`.tif`) as output.
6. Do not select “Create world file only”.
7. Start georeferencing.
8. Open the resulting GeoTIFF in Map2Device.

Good control points include road intersections, bridges, buildings, lift stations, peaks and other clearly identifiable features. Highly distorted tourist or piste maps may not align accurately over the entire image.

## Compatibility and feedback

See [COMPATIBILITY.md](COMPATIBILITY.md) for the current profile list.

Hardware reports and bug reports are especially useful during the Public Beta:

[Open GitHub Issues](https://github.com/gridovate-motion/Map2Device/issues)

Please include device model, firmware, input format, whether the map is detected, position accuracy, zoom behaviour and any rendering issues.

## Windows SmartScreen

Map2Device v0.30 Public Beta is currently **not digitally signed**. Windows may therefore display “Unknown publisher” or “Windows protected your PC”. A SHA-256 checksum is provided with every official release.

## Beta lifetime

This Public Beta is enabled until **31 January 2027**. After that date, a current build is required.

## Map rights and trademarks

Map2Device does not include maps or imagery. Users are responsible for ensuring that they have the necessary rights to use and convert their source material.

Garmin and Garmin product names are trademarks of Garmin Ltd. or its subsidiaries. TwoNav and Land are trademarks or product names of their respective owners.

**Map2Device by Gridovate Motion is an independent project and is not affiliated with, sponsored by, endorsed by or tested by Garmin Ltd., TwoNav or CompeGPS.** Brand and product names are used solely to describe compatibility.

## Privacy

Map conversion is performed locally on the computer. This build does not require a user account and does not upload map data to Garmin, TwoNav or Gridovate Motion.

## Version

**Map2Device v0.30 Public Beta · November 2026**  
Developer / publisher: **Gridovate Motion**  
Copyright © 2026 Gridovate Motion. All rights reserved.
