# Decisions — Ablauf-Entscheidungen

Dokumentation bewusster Ablauf-Anpassungen („was habe ich am Vorgehen geändert").

## 1. Pfad-Disziplin: git ist die einzige Autorität
- **Problem:** Es existieren zwei fast identische Verzeichnisse
  (`HornissenFindAppPrototyp` ↔ `HornissenFindAppPrototyp`) und zwei User-Pfade
  (`MaikKlingert` ↔ `MaikKlingert`). Raten führte zu Edits in der falschen Kopie.
- **Entscheidung:** Repo-Root ausschließlich über `git rev-parse --show-toplevel`
  bestimmen, alle Edits relativ dazu (`Prototyp/index.html`). Arbeitskopie = getrackte Datei.

## 2. Code vor Board, Beweis vor Status
- **Entscheidung:** Eine Card wird erst auf „Done" gesetzt, wenn es einen **Selbsttest-
  Beweis** gibt, der im `selfTest()` live läuft (und idealerweise am Live-Deploy verifiziert).
  Board-Status-Sync ist Folgearbeit, nicht Selbstzweck.

## 3. Ein Board-Dump pro Entscheidung (keine Parallel-Mutationen)
- **Problem:** Mehrere parallele GraphQL-Requests vermischten Item-IDs; Substring-Matching
  (`id.Length -ge 40 ? …`) scheiterte an PowerShell-5.1-Parser.
- **Entscheidung:** Board-Zustand + Status-Option-IDs (fid/oid) **aus demselben** Request
  holen; Mutation ausschließlich mit diesen IDs. Kein Ternär in PowerShell (5.1 kennt ihn nicht).

## 4. Selbsttests im Browser, nicht per Node
- Kein Node.js verfügbar; `selfTest()` läuft nur clientseitig. Verifikation daher über
  Commit/ Push / Live-Pages-Inhalt statt lokaler Ausführung.

## 5. Inhaltliche Skalierung: Share-Feature
- „Teilen mit Backend" ist auf statischem GitHub Pages ohne externen Dienst nicht machbar.
  → Scope-Entscheidung nötig (siehe ToDo.md), nicht stillschweigend „Done" melden.
