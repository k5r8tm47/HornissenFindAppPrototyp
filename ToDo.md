# ToDo — HornissenFindApp (Prototyp) — offene Cards

Ehrlicher Code-/Board-Abgleich (nicht rückwärts aus dem Board geraten).

## Offene Aufgaben (Board = Backlog, Stand letzter verlässlicher Dump)

### 1. Sichtungen teilen: echtes Backend bzw. Multi-User-Sync  [Card `6gRxU`]
- **STATUS: offen (Backlog)** — nicht implementiert.
- Grund: GitHub Pages ist statisch, es gibt kein Server-Backend. „Teilen" braucht
  einen externen Dienst (Firebase/Supabase/API-Gateway) ODER einen Share-Link-Ansatz
  (URL mit kodierten Sichtungsdaten).
- Nächster Schritt: Scope klären — (a) Share-Link ohne Backend, oder (b) echtes
  Backend. Erst nach Entscheidung implementieren.

### 2. Offline-Karten-Caching: OSM-Tiles als Fallback für den Feld-Einsatz  [Card `6gRw8`]
- **Code-Stand:** `sw.js` existiert, cached OSM-Assets, network-first + `caches.match`-Fallback,
  Registrierung live im HTML (Z.1094) — **Ansatz vorhanden**.
- **Offen:** Verifikation/Beweis auf dem Feld-Betrieb + evtl. Tile-Liste erweitern.
- Nächster Schritt: Selbsttest-Beweis ergänzen (Cache gefüllt → Offline-Fallback liefert Tile).

### 3. Strichlänge: max. 800 m überprüfen bzw. konfigurierbar machen  [Card `6gRxs`]
- **Code-Stand:** `LINE_M = 800` + `effLine()` begrenzt überall; `effLen` im selfTest.
- **Offen (fakultativ):** konfigurierbar machen (Admin-Einstellung statt Konstante).
  Die harte 800-m-Grenze ist implementiert; nur die Konfigurierbarkeit fehlt.

## Erledigt & live (zur Einordnung, aus Git + Live-Pages belegt)
- Kartenansicht (OSM), Sichtung erfassen, Admin-Ansicht, 800-m-Strich, lokale Speicherung,
  Export/Import, PWA-Grundgerüst, Responsives Layout, Teilen an Admin, Triangulation,
  Google-Maps-Link + rote Hinweis-Benachrichtigung, Nestbereich-Status, Flugzeit-Eingabe
  verkürzt Strich, Protokoll, Bottom-Sheet-Formular, Standort/Flugrichtung per langem Drücken,
  durchgezogener Strich, Pfeil, XSS-Hygiene (`escapeHtml` überall), localStorage-Limit (try/catch).
- **Hinweis:** Einige dieser Punkte stehen im Board fälschlich als Backlog/In Progress, obwohl
  der Code committed + live ist (Board-Sync-Defizit) — Status-Abgleich ist Teil der Arbeit.
