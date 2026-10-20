# Outdoor Map Converter

**Bring your own raster maps to Garmin and TwoNav devices.**

Developed by **Gridovate Motion**

[![Download for Windows](https://img.shields.io/badge/Download_for_Windows-v0.29_Public_Beta-0078D4?style=for-the-badge&logo=windows)](https://github.com/gridovate-motion/Outdoor-Map-Converter/releases/download/v0.29-public-beta/Outdoor_Map_Converter_v029_Public_Beta.exe)

**Windows 10/11 · 64-bit · Portable · No installation required**

> **Public Beta**
>
> This beta is valid until **31 January 2027**.
>
> Outdoor Map Converter is currently distributed as an unsigned application.  
> Windows SmartScreen may therefore display an **"Unknown publisher"** warning.
>
> Please download the application only from the official Gridovate Motion GitHub repository.

[View release notes and SHA-256 checksum](https://github.com/gridovate-motion/Outdoor-Map-Converter/releases/tag/v0.29-public-beta)

**Deutsch:** [README_DE.md](README_DE.md)

---

## What is Outdoor Map Converter?

Outdoor Map Converter converts georeferenced raster maps into formats that can be displayed on supported **Garmin** and **TwoNav** devices.

The idea is simple:

**Your map → Outdoor Map Converter → your GPS device**

You can use your own topographic maps, city maps, ski resort maps, aerial imagery, historical maps or other georeferenced raster maps and carry them directly on your outdoor GPS device or compatible sports watch.

### Supported input

- GeoTIFF (`.tif`, `.tiff`)
- legacy GeoGrid / Austrian Map PDA files (`.mph` / `.mpr`)

### Supported output

- **Garmin Custom Maps:** KMZ
- **TwoNav:** MBTiles

The application automatically prepares the map according to the selected device profile.

---

## Why use your own maps?

Outdoor Map Converter is not limited to traditional hiking maps.

Any suitable raster map can potentially be used if it is correctly georeferenced.

### Ski resort maps

A georeferenced piste map can be displayed directly on a compatible Garmin or TwoNav device.

This allows you to see your current GPS position on the familiar ski resort map without having to take out your phone.

### City maps

A detailed city or tourist map can be prepared for your GPS device and used while exploring attractions, streets and districts.

### Aerial imagery

Georeferenced aerial photographs can be useful for:

- outdoor navigation
- forestry
- agriculture
- terrain orientation
- local exploration

### Historical maps

Old maps can be georeferenced and compared with your current GPS position.

This can be useful for exploring:

- former roads
- old buildings
- historical boundaries
- abandoned infrastructure
- landscape changes

### Other possible uses

- hiking maps
- orientation maps
- cycling maps
- event areas
- large parks
- university campuses
- camping grounds
- recreational areas
- custom local maps

---

## Quick start

### 1. Download Outdoor Map Converter

Download the latest Public Beta:

**[Download Outdoor Map Converter v0.29 Public Beta for Windows](https://github.com/gridovate-motion/Outdoor-Map-Converter/releases/download/v0.29-public-beta/Outdoor_Map_Converter_v029_Public_Beta.exe)**

No installation is required.

Simply start:

`Outdoor_Map_Converter_v029_Public_Beta.exe`

---

### 2. Select your source map

Choose a supported map file:

- GeoTIFF
- GeoGrid `.mph`
- GeoGrid `.mpr`

For GeoGrid maps, keep the corresponding `.mph` and `.mpr` files together.

---

### 3. Select manufacturer and device

Choose:

- Garmin
- TwoNav

and then select your device model.

Outdoor Map Converter uses device-specific profiles where available.

A manual profile is also available for unsupported or experimental devices.

---

### 4. Choose an output location

Select where the converted map should be saved.

A manually selected output folder always has priority.

---

### 5. Create the map

Start the conversion.

Outdoor Map Converter automatically creates the appropriate output format:

| Target | Output |
|---|---|
| Garmin | `.kmz` |
| TwoNav | `.mbtiles` |

---

### 6. Copy the map to your device

#### Garmin

Garmin Custom Maps are normally copied to:

`Garmin\CustomMaps`

The exact location may depend on the device.

#### TwoNav

TwoNav maps are normally stored in:

`TwoNavData\Maps`

---

## Do I need a georeferenced map?

Yes.

Outdoor Map Converter currently expects the raster map to already contain geographic information.

If you only have a normal JPG, PNG, scan, city map or ski resort map, it must first be georeferenced.

The easiest free option is **QGIS**.

---

## Simple georeferencing with QGIS

You do not need advanced GIS knowledge for basic maps.

### Basic workflow

1. Install QGIS.
2. Open the **Georeferencer**.
3. Load your map image.
4. Add several clearly identifiable control points.
5. Assign the corresponding real-world coordinates.
6. Select **GeoTIFF** as the output format.
7. Start the georeferencing process.
8. Open the resulting `.tif` file in Outdoor Map Converter.

### Good control points include

For city maps:

- road intersections
- prominent buildings
- bridges
- squares

For ski resort maps:

- valley stations
- mountain stations
- lift intersections
- prominent peaks
- clearly identifiable buildings

For aerial imagery:

- road intersections
- building corners
- bridges
- distinctive terrain features

### Recommendation

Use at least **four well-distributed control points** whenever possible.

Avoid placing all control points in the same small area of the map.

---

## Important note about illustrated maps

Some tourist maps and ski resort maps are intentionally distorted for better readability.

For example, slopes, mountains or distances may be visually enlarged or moved.

Such maps can still sometimes be georeferenced, but GPS alignment may vary across the map.

Maps that are geographically or proportionally accurate will generally provide better results.

---

## Garmin support

Outdoor Map Converter creates Garmin Custom Maps as KMZ files.

Device profiles contain appropriate map limits and settings where known.

### Hardware tested

**Garmin Forerunner 970**

Garmin KMZ export has been successfully tested on real hardware.

Support for additional Garmin devices is based on documented Custom Maps capabilities and device profiles.

Community hardware feedback is welcome.

See:

[COMPATIBILITY.md](COMPATIBILITY.md)

---

## TwoNav support

Outdoor Map Converter creates raster MBTiles for TwoNav devices.

### Software tested

TwoNav MBTiles output has been successfully tested in:

**TwoNav Land**

Hardware testing on additional TwoNav GPS devices is especially welcome.

Supported profiles currently include devices from the:

- Aventura family
- Cross family
- Roc
- Terra
- Trail family

See:

[COMPATIBILITY.md](COMPATIBILITY.md)

---

## Hardware testing wanted

One of the main goals of the Public Beta is to verify compatibility with as many devices as possible.

If you own a supported Garmin or TwoNav device, your feedback is very valuable.

Please report:

- manufacturer
- device model
- firmware version
- whether the map is detected
- whether the map is displayed correctly
- whether GPS position alignment is correct
- whether zoom levels work
- whether missing or white areas appear

Use:

**Issues → New issue → Hardware compatibility report**

[Open Issues](https://github.com/gridovate-motion/Outdoor-Map-Converter/issues)

---

## Found a bug?

Please create a GitHub issue using the **Bug report** template.

Useful information includes:

- Outdoor Map Converter version
- Windows version
- input format
- selected device
- error message
- steps required to reproduce the problem
- screenshot if available

[Report a bug](https://github.com/gridovate-motion/Outdoor-Map-Converter/issues)

---

## Windows SmartScreen

Outdoor Map Converter v0.29 Public Beta is currently **not digitally signed**.

Windows may therefore display messages such as:

- "Unknown publisher"
- "Windows protected your PC"

This does not automatically mean that the application is malicious. Windows displays these warnings for unsigned or low-reputation applications.

For security, download Outdoor Map Converter only from the official Gridovate Motion GitHub release.

A SHA-256 checksum is provided with every official release.

### Verify the checksum

The official checksum is available in:

`SHA256SUMS.txt`

on the GitHub Release page.

---

## Public Beta status

Current version:

**v0.29 Public Beta**

Beta expiration:

**31 January 2027**

The beta period is intended to collect:

- device compatibility reports
- export issues
- map rendering problems
- usability feedback
- ideas for future features

Future versions may change file handling, device profiles or supported formats.

---

## Planned ideas

Possible future development includes:

- simplified built-in georeferencing
- additional device profiles
- additional raster formats
- improved compatibility validation
- easier workflows for city maps and ski resort maps
- expanded hardware testing

Features are not guaranteed and will depend on testing and feedback.

---

## Map rights and copyright

Outdoor Map Converter does **not** include maps, aerial imagery, ski resort maps or other copyrighted map material.

Users are responsible for ensuring that they have the necessary rights to:

- use
- convert
- store
- distribute

their source maps and imagery.

Only convert material that you are legally permitted to use.

---

## Trademark notice

Garmin and Garmin product names are trademarks of Garmin Ltd. or its subsidiaries.

TwoNav and Land are trademarks or product names of their respective rights holders.

**Outdoor Map Converter is an independent project developed by Gridovate Motion and is not affiliated with, sponsored by, endorsed by or associated with Garmin Ltd., TwoNav or CompeGPS.**

Brand and product names are used solely to describe compatibility with the respective devices and file formats.

---

## License

Outdoor Map Converter v0.29 is distributed under the Public Beta license included in this repository.

See:

[BETA_LICENSE.txt](BETA_LICENSE.txt)

Copyright © 2026 **Gridovate Motion**.  
All rights reserved.

---

## Changelog

See:

[CHANGELOG.md](CHANGELOG.md)

---

## Compatibility

Known and planned device compatibility:

[COMPATIBILITY.md](COMPATIBILITY.md)

---

## Feedback

Feedback, hardware test results and bug reports are welcome through GitHub Issues.

**Gridovate Motion**

Outdoor Map Converter is currently an independent Public Beta project.
