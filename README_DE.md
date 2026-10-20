# Outdoor Map Converter v0.29 Public Beta RC1

**Eigene Rasterkarten auf Garmin- und TwoNav-Geräten verwenden.**

**Entwickelt von Gridovate Motion**

Outdoor Map Converter konvertiert georeferenzierte Rasterkarten automatisch in das passende Ausgabeformat für das gewählte Gerät:

- **Garmin** → KMZ / Garmin Custom Maps
- **TwoNav** → Raster-MBTiles

Zusätzlich kann das Programm ältere **AMap/GeoGrid-PDA-Karten (`.mph` + `.mpr`)** direkt verarbeiten.

> **Public Beta RC1:** gültig bis **31.01.2027**. Diese Vorabversion dient dem Test auf möglichst vielen Geräten.

## Wofür kann ich das verwenden?

Nicht nur klassische Wanderkarten sind möglich. Grundsätzlich eignet sich jede sinnvoll georeferenzierbare Rasterkarte, zum Beispiel:

- topografische Karten und Wanderkarten
- **Pistenpläne von Skigebieten**, damit die eigene GPS-Position direkt am Handgelenk oder auf dem GPS-Gerät sichtbar ist
- **Stadtpläne** für Reisen und Sightseeing
- Luftbilder und Orthofotos
- historische Karten
- Orientierungslaufkarten
- Gelände-, Campus-, Freizeitpark- oder Veranstaltungspläne
- selbst erstellte maßstabsgetreue Karten

Wichtig: Ein Rasterbild wird dadurch **nicht routingfähig**. Straßen, Lifte oder Sehenswürdigkeiten werden nicht automatisch zu anklickbaren POIs. Das Gerät zeigt aber die eigene GPS-Position auf der georeferenzierten Karte an.

## Unterstützte Eingaben

- GeoTIFF (`.tif`, `.tiff`) mit eingebetteter Georeferenzierung
- AMap/GeoGrid-PDA-Export (`.mph` + `.mpr`)

Ein normales JPG/PNG ohne Georeferenzierung muss derzeit zuerst georeferenziert und als GeoTIFF gespeichert werden. Ein eigener Georeferenzierer ist für eine spätere Version geplant, aber **nicht Bestandteil dieser Beta**.

## Installation unter Windows

1. Release-ZIP herunterladen und entpacken.
2. `Outdoor_Map_Converter_v029_Public_Beta.exe` starten.
3. Sprache oben rechts auf **Deutsch** oder **English** stellen.

Für diese Windows-Version ist keine Python-Installation erforderlich.

Die Public Beta ist derzeit **nicht digital signiert**. Windows SmartScreen kann deshalb bei einer neu heruntergeladenen EXE eine Warnung anzeigen. Die Datei sollte nur aus dem offiziellen Projekt-Release gestartet werden. Optional kann die SHA-256-Prüfsumme mit `SHA256SUMS.txt` verglichen werden.

## Bedienung

1. **Eingabe auswählen**: GeoTIFF oder `.mph` einer AMap/GeoGrid-PDA-Karte.
2. Kartenname prüfen oder ändern.
3. **Zielgerät** aus der alphabetischen Geräteliste wählen.
4. Qualität wählen. Für sehr große Garmin-Karten kann `Großgebiet (Auto)` sinnvoll sein.
5. Ausgabeort prüfen oder über **Speichern als …** selbst wählen.
6. **Garmin-KMZ erstellen** bzw. **TwoNav-MBTiles erstellen** anklicken.
7. Nach Abschluss die fertige Datei auf das Gerät kopieren.

Ein manuell gewählter Ausgabeordner hat immer Vorrang und wird vom Programm nicht mehr automatisch überschrieben.

## Garmin

Für Garmin erzeugt das Programm eine Custom-Map-KMZ mit `doc.kml` und nicht-progressiven JPEG-Kacheln. Das Kachellimit wird automatisch anhand des ausgewählten Geräteprofils gesetzt.

Typischer Zielordner auf dem Gerät:

`Garmin\CustomMaps`

Die Forerunner 970 wurde im Projekt praktisch getestet. Weitere Profile basieren auf Garmin-Dokumentation bzw. klar gekennzeichneten Praxisquellen.

## TwoNav

Für TwoNav wird automatisch eine Raster-MBTiles-Datei erzeugt. Das Garmin-Kachellimit gilt hier nicht.

Typischer Zielordner auf dem Gerät:

`TwoNavData\Maps`

Der erzeugte MBTiles-Export wurde mit **TwoNav Land unter Windows erfolgreich getestet**. Hardwaretests auf echten TwoNav-Geräten sind ausdrücklich erwünscht.

## Noch keine georeferenzierte Karte? Einfache Lösung mit QGIS

Für Stadtpläne, Pistenpläne, Luftbilder oder gescannte Karten ist QGIS derzeit der einfachste kostenlose Weg.

### Kurz-Anleitung

1. QGIS installieren.
2. **Raster → Georeferenzierer** öffnen.
3. Bild oder Scan laden.
4. Mindestens 3 bis 4 gut verteilte, eindeutig erkennbare Passpunkte setzen.
5. Den Punkten ihre korrekten Koordinaten zuweisen bzw. sie über die QGIS-Karte bestimmen.
6. Unter **Transformationseinstellungen** als Ausgabedatei ein `.tif` wählen.
7. **Nur World-Datei erzeugen** nicht aktivieren.
8. Ein Ziel-KBS festlegen. Der Outdoor Map Converter übernimmt später die nötige Umprojektion.
9. Georeferenzierung starten.
10. Das fertige GeoTIFF im Outdoor Map Converter öffnen.

### Gute Passpunkte

- Stadtplan: Kreuzungen, Brücken, markante Gebäude
- Pistenplan: Talstationen, Bergstationen, Gipfel, markante Liftkreuzungen
- Luftbild: Straßenkreuzungen, Gebäude, Geländepunkte
- historische Karte: heute noch eindeutig identifizierbare Punkte

Die Punkte sollten über die ganze Karte verteilt sein. Rein illustrative oder stark perspektivisch verzerrte Pistenpläne können nur eingeschränkt exakt georeferenziert werden.

## Hardwaretests und Feedback

Für die Public Beta sind besonders Tests auf unterschiedlichen Garmin- und TwoNav-Modellen hilfreich. Bitte bei einer Rückmeldung angeben:

- Hersteller und Modell
- Firmware-Version
- Karte erkannt: Ja/Nein
- Position korrekt: Ja/Nein
- Zoomen vollständig: Ja/Nein
- weiße Bereiche oder Darstellungsfehler
- Geschwindigkeit / Abstürze / sonstige Auffälligkeiten

Siehe auch `HARDWARE_TEST_FEEDBACK.md`.

## Beta-Laufzeit

Diese Public Beta ist bis **31.01.2027** freigeschaltet. Danach ist eine aktuelle Version erforderlich. Die zeitliche Begrenzung dient dazu, dass veraltete Testversionen nicht dauerhaft weiterverwendet werden.

## Rechtlicher Hinweis

Garmin und die Bezeichnungen der Garmin-Produkte sind Marken von Garmin Ltd. oder deren Tochtergesellschaften. TwoNav und Land sind Marken bzw. Produktbezeichnungen ihrer jeweiligen Rechteinhaber.

**Outdoor Map Converter wird unabhängig von Gridovate Motion entwickelt und steht in keiner Verbindung zu Garmin Ltd. oder TwoNav/CompeGPS. Das Projekt wird von diesen Unternehmen weder unterstützt noch geprüft.** Die Marken werden ausschließlich verwendet, um die Kompatibilität des Programms zu beschreiben.

Der Nutzer ist selbst dafür verantwortlich, nur Karten, Luftbilder, Pläne oder sonstige Daten zu konvertieren, für die die erforderlichen Nutzungsrechte bestehen. Das Programm enthält keine Karteninhalte von Garmin, TwoNav, BEV oder anderen Kartenanbietern.

## Datenschutz

Die Konvertierung erfolgt lokal auf dem Computer. Diese Version benötigt für die Kartenkonvertierung keine Benutzerkonten und überträgt keine Kartendaten an Garmin, TwoNav oder Gridovate Motion.

## Versionsstand

v0.29 Public Beta RC1, Oktober 2026  
Entwicklung / Herausgeber: **Gridovate Motion**  
Copyright © 2026 Gridovate Motion. All rights reserved.
