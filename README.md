# HornissenFindApp Prototyp

Web-App (PWA) für Imker, um Hornissen-Nester rund um den eigenen Bienenstand zu lokalisieren.

## Funktionen (Prototyp)

- **Kartenansicht** mit Bienenstand-Marker und visualisiertem Flugradius (~1 km)
- **Bienenstände** anlegen, benennen und per Klick auf der Karte positionieren
- **Sichtungen markieren**: Hornissen-Sichtungen per Klick als Marker mit Datum und Notiz erfassen
- **Sichtungen verwalten**: Liste, Bearbeiten und Löschen
- **Lokale Datenspeicherung** im Browser (localStorage/IndexedDB) – keine Datenverluste nach Neustart
- **Export/Import** als JSON-Datei (Sicherung und Gerätewechsel)
- **PWA**: installierbar auf dem Smartphone, offline nutzbar
- **Responsives Layout** für Mobile (Touch) und Desktop

## Technik

- Reine Web-App ohne Backend; alle Daten liegen lokal im Browser
- Karten: [Leaflet](https://leafletjs.com) mit OpenStreetMap-Tiles (Kartenanbieter später austauschbar, z. B. Google Maps)
- PWA via Manifest + Service Worker

## Projektverwaltung

Entwicklungsaufgaben werden im GitHub-Projekt [HornissenFindApp Prototyp - Entwicklung](https://github.com/users/k5r8tm47/projects/2) mit den Spalten Backlog / To Do / In Progress / In Review / Done geführt.

## Status

Prototyp in Planung – noch kein Code.