# Suggestions — Verbesserungsvorschläge am Ablauf

## S1. Board-Sync als eigenständiges, verifizierbares Skript
Mutationen/Dumps immer wieder per Hand in Bash → fehleranfällig (PowerShell-5.1-IDs,
Substring-Fallen). Vorschlag: Ein `board-sync.ps1` mit fest vordefinierten, **aus dem
Board gelesenen** fid/oid-Mappings + Prüf-Dump, damit Done-Setzungen reproduzierbar sind.
(Hinweis: nicht committen — nur lokal, als Arbeitshilfe.)

## S2. Selbsttest-Fläche im UI erweitern
Der `selfTest()`-Block wächst; Vorschlag: Ausgaben nicht nur in ein `<pre>`, sondern als
Liste mit Gründe-Attribut („warum gilt diese Card als erfüllt?"), damit Review ohne
Quelltext-Suche möglich ist.

## S3. „Done"-Definition im Workflow explizit machen
Klarstellen: Done = Code committed + gepusht + Live-Pages enthält den Selbsttest-Beweis.
Das beugt dem beobachteten Board-Sync-Defizit vor (Cards Done im Code, aber Backlog im Board).

## S4. Backend-Entscheidung früh klären
„Sichtungen teilen" (Card `6gRxU`) blockiert ohne externe Infrastruktur. Empfehlung:
Entscheidung Share-Link (kein Backend) vs. echtes Backend, **bevor** weitere Feld-Cards
gebaut werden — sonst bleibt ein endloser Prototyp ohne Teilen-Funktion.

## S5. Keine Artefakte im Commit
Lesen/Schreiben nur an getrackten Dateien; Temp-/Hilfsdateien (`board.json`, `check.ps1`)
vor dem Push löschen bzw. außerhalb des Repos halten — hatte in der Vergangenheit zu
Verwirrung (falsche Pfade, ungewollte Untracked-Dateien) geführt.
