# Umsetzungs-Prompt: HornissenFindApp Prototyp

Setze die offenen Issues des GitHub-Projekts **HornissenFindApp Prototyp - Entwicklung** um:

https://github.com/users/k5r8tm47/projects/2

## Kontext

- Repo: https://github.com/k5r8tm47/HornissenFindAppPrototyp
- Live-App (GitHub Pages): https://k5r8tm47.github.io/HornissenFindAppPrototyp/
- Code liegt im Ordner `Prototyp/`; Deployment über `.github/workflows/pages.yml` (GH Actions, push auf `main`)
- Der Prototyp ist eine reine Client-App ohne Backend: eine `index.html` (Leaflet + OpenStreetMap), Daten in `localStorage`

## Produkt-Konzept (unveränderlich)

- Zielgruppe: Imker
- Methode: Fangort der asiatischen Hornisse auf der Karte markieren → Hornisse freilassen → Flugrichtung direkt auf der Karte angeben
- Die Karte zeichnet vom Fangpunkt einen Pfeil in Flugrichtung; mehrere Fänge überlagern sich und zeigen die Richtung zum Nest
- **Kein Bienenstand nötig** - dafür gibt es keine Funktion

## Vorgehen

1. Lies zuerst die Projekt-Spalten (Backlog / To Do / In Progress / In Review / Done) und lies die aktuellen Issues samt Bodies.
2. Nimm Issues in sinnvoller Reihenfolge aus `Backlog`/`To Do`, setze sie in der Umsetzung auf `In Progress`.
3. Implementiere, teste lokal (Datei im Browser öffnen), committe und pushe.
4. Setze das Issue danach auf `In Review` bzw. nach Verifikation auf `Done` - der Status im Projekt muss dem Stand entsprechen.

## Umsetzungsregeln

- Nur eine `index.html` ohne Build-Schritt, solange sinnvoll (kein Framework erforderlich)
- Keep it simple: keine ungefragten Abstraktionen, keine zusätzlichen Dependencies
- Deutschsprachige UI, Commit-Meldungen auf Englisch
- Bestehen lokale Daten weiterhin in `localStorage` unter einem stabilen Key
- Nach jedem Push prüfen, ob der GitHub-Actions-Workflow und die Live-URL fehlerfrei deployen