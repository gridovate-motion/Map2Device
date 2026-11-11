# Map2Device

**Rasterkarten optimiert für Uhren und Outdoor-GPS-Geräte.**

**by Gridovate Motion**

[![Download für Windows](https://img.shields.io/badge/Download_f%C3%BCr_Windows-v0.30_Public_Beta-0B5ED7?style=for-the-badge&logo=windows)](https://github.com/gridovate-motion/Map2Device/releases/download/v0.30-public-beta/Map2Device_v030_Public_Beta.exe)

**Windows 10/11 · 64 Bit · portabel · keine Installation erforderlich**

> **Public Beta:** gültig bis **31.01.2027**. Map2Device ist derzeit nicht digital signiert. Windows SmartScreen kann deshalb eine Warnung wegen eines unbekannten Herausgebers anzeigen. Bitte nur über den offiziellen GitHub-Release von Gridovate Motion herunterladen.

[Release-Seite und Prüfsumme](https://github.com/gridovate-motion/Map2Device/releases/tag/v0.30-public-beta) · **English:** [README.md](README.md)

---

## Was ist Map2Device?

Map2Device bereitet georeferenzierte Rasterkarten für kompatible **Garmin-** und **TwoNav-Geräte** auf. Es wird nicht nur ein Dateiformat gewechselt: Die Karte wird gerätegerecht gekachelt und hinsichtlich Auflösung, Dateigröße und bekannten Geräte-Limits für das gewählte Ziel aufbereitet.

**Map → Device**

Aktuelle Ausgabe:
- **Garmin** → KMZ / Garmin Custom Maps
- **TwoNav** → Raster-MBTiles

Unterstützte Eingaben:
- GeoTIFF (`.tif`, `.tiff`) mit eingebetteter Georeferenzierung
- ältere AMap-/GeoGrid-PDA-Karten (`.mph` + `.mpr`)

## Typische Anwendungen

Map2Device kann mit vielen Arten georeferenzierter Rasterkarten verwendet werden, zum Beispiel:
- Orientierungslaufkarten
- Wander- und topografische Karten
- Pistenpläne von Skigebieten
- Stadt- und Touristenpläne
- Luftbilder und Orthofotos
- historische Karten
- Campus-, Park-, Veranstaltungs- oder Geländepläne

Die Karte bleibt eine Rasterkarte. Straßen, Lifte oder POIs werden nicht automatisch routingfähig oder interaktiv. Das Gerät kann jedoch die eigene GPS-Position auf der georeferenzierten Karte darstellen.

## Schnellstart

1. `Map2Device_v030_Public_Beta.exe` herunterladen.
2. EXE starten. Eine Installation ist nicht erforderlich.
3. GeoTIFF oder die `.mph`-Datei einer AMap/GeoGrid-PDA-Karte auswählen.
4. Zielgerät wählen oder **Manuell / anderes Gerät** verwenden.
5. Qualität und Ausgabeort wählen.
6. Garmin-KMZ bzw. TwoNav-MBTiles erstellen.
7. Fertige Datei auf das Gerät kopieren.

Ein manuell gewählter Ausgabeordner hat immer Vorrang.

## Garmin

Für Garmin erzeugt Map2Device eine Custom-Map-KMZ mit `doc.kml` und nicht-progressiven JPEG-Kacheln. Bekannte Kachellimits werden automatisch aus dem gewählten Geräteprofil übernommen.

Typischer Zielordner:

`Garmin\CustomMaps`

Die **Forerunner 970** wurde im Projekt auf echter Hardware getestet. Weitere Profile basieren auf Herstellerdokumentation oder klar gekennzeichneten Praxisquellen. Über die manuelle Auswahl können zusätzliche Geräte getestet werden.

## TwoNav

Für TwoNav erzeugt Map2Device Raster-MBTiles. Garmin-Kachellimits gelten dort nicht.

Typischer Zielordner:

`TwoNavData\Maps`

Der erzeugte MBTiles-Export wurde in **TwoNav Land unter Windows erfolgreich getestet**. Rückmeldungen von echten TwoNav-Geräten sind ausdrücklich erwünscht.

## Noch keine georeferenzierte Karte?

Für JPG/PNG, Scans, Stadtpläne oder Pistenpläne ohne Georeferenzierung ist **QGIS** derzeit der empfohlene kostenlose Weg.

### Einfache QGIS-Georeferenzierung
1. **Raster → Georeferenzierer** öffnen.
2. Bild oder Scan laden.
3. Mindestens 3–4 gut verteilte Passpunkte setzen.
4. Den Punkten die passenden realen Koordinaten zuweisen.
5. GeoTIFF (`.tif`) als Ausgabe wählen.
6. „Nur World-Datei erzeugen“ nicht aktivieren.
7. Georeferenzierung starten.
8. Das fertige GeoTIFF in Map2Device öffnen.

Gute Passpunkte sind etwa Kreuzungen, Brücken, Gebäude, Liftstationen, Gipfel und andere eindeutig erkennbare Stellen. Stark verzerrte touristische Karten oder Pistenpläne können über die gesamte Fläche weniger genau sein.

## Kompatibilität und Feedback

Die aktuelle Geräteliste steht in [COMPATIBILITY.md](COMPATIBILITY.md).

Hardwaretests und Bug Reports sind während der Public Beta besonders hilfreich:

[GitHub Issues öffnen](https://github.com/gridovate-motion/Map2Device/issues)

Bitte nach Möglichkeit Gerät, Firmware, Eingabeformat, Kartenerkennung, Positionsgenauigkeit, Zoomverhalten und Darstellungsfehler angeben.

## Windows SmartScreen

Map2Device v0.30 Public Beta ist derzeit **nicht digital signiert**. Windows kann deshalb „Unbekannter Herausgeber“ oder „Der Computer wurde durch Windows geschützt“ anzeigen. Zu jedem offiziellen Release wird eine SHA-256-Prüfsumme bereitgestellt.

## Beta-Laufzeit

Diese Public Beta ist bis **31.01.2027** freigeschaltet. Danach ist eine aktuelle Version erforderlich.

## Kartenrechte und Marken

Map2Device enthält keine Karten oder Luftbilder. Nutzer sind selbst dafür verantwortlich, nur Material zu verwenden und zu konvertieren, für das die erforderlichen Rechte bestehen.

Garmin und die Bezeichnungen der Garmin-Produkte sind Marken von Garmin Ltd. oder deren Tochtergesellschaften. TwoNav und Land sind Marken bzw. Produktbezeichnungen ihrer jeweiligen Rechteinhaber.

**Map2Device by Gridovate Motion ist ein unabhängiges Projekt und steht in keiner Verbindung zu Garmin Ltd., TwoNav oder CompeGPS. Das Projekt wird von diesen Unternehmen weder unterstützt noch geprüft.** Die Markennamen werden ausschließlich zur Beschreibung der Kompatibilität verwendet.

## Datenschutz

Die Kartenkonvertierung erfolgt lokal auf dem Computer. Diese Version benötigt kein Benutzerkonto und überträgt keine Kartendaten an Garmin, TwoNav oder Gridovate Motion.

## Versionsstand

**Map2Device v0.30 Public Beta · November 2026**  
Entwicklung / Herausgeber: **Gridovate Motion**  
Copyright © 2026 Gridovate Motion. All rights reserved.
