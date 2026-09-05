# HornissenFindApp Prototyp

Web-App (PWA) für Imker zur Ortung von Nestern der asiatischen Hornisse über die Flugrichtung freigelassener Hornissen.

## Funktionsprinzip

1. Asiatische Hornisse in der Nähe der Bienenvölker fangen
2. **Fangort** auf der Karte markieren (Klick auf die Karte, mit Datum/Notiz)
3. Hornisse kennzeichnen und freilassen
4. **Flugrichtung** direkt auf der Karte angeben (Klick in die Richtung, in die die Hornisse abfliegt)

Vom Fangpunkt wird ein Pfeil in Flugrichtung gezeichnet. Mehrere Fänge von verschiedenen Standorten überlagern sich und zeigen so die Richtung zum Nest.

Ein Bienenstand ist für dieses Vorgehen nicht erforderlich.

## Funktionen (Prototyp)

- **Kartenansicht** (OpenStreetMap, Leaflet)
- **Fangort setzen** per Klick auf die Karte (mit Datum/Notiz)
- **Flugrichtung festlegen** per Klick, Pfeil vom Fangpunkt in Flugrichtung
- **Fänge verwalten**: Liste, Bearbeiten der Flugrichtung, Löschen
- **Lokale Datenspeicherung** im Browser (localStorage) – bleibt nach Neustart erhalten
- **Responsives Layout** für Mobile (Touch) und Desktop

## Live-Demo

[https://k5r8tm47.github.io/HornissenFindAppPrototyp/](https://k5r8tm47.github.io/HornissenFindAppPrototyp/)

## Technik

- Reine Web-App ohne Backend; alle Daten liegen lokal im Browser
- Karten: [Leaflet](https://leafletjs.com) mit OpenStreetMap-Tiles (Kartenanbieter später austauschbar, z. B. Google Maps)
- Deployment auf GitHub Pages per GitHub Actions (Quellordner: `Prototyp/`)

## Projektverwaltung

Entwicklungsaufgaben werden im GitHub-Projekt [HornissenFindApp Prototyp - Entwicklung](https://github.com/users/k5r8tm47/projects/2) mit den Spalten Backlog / To Do / In Progress / In Review / Done geführt.

## Status

Funktionierender Mini-Prototyp (eine `index.html` ohne Build-Schritt).