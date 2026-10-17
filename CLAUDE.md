# ClassroomSpark

## Was das ist
- Landingpage für Lehrkräfte, die die interaktiven Trainer und
  fachübergreifenden Werkzeuge vorstellt.
- Besteht aus index.html (+ `downloads/` für Begleitmaterial). Die Werkzeuge selbst liegen in:
  - `training` — fachspezifische Trainer (English/Chemistry).
  - `tools` — fachübergreifende Werkzeuge (General Tools) und der neutrale
    Arduino-Uploader (Computer Science, `tools/arduino-upload.html`).
  - Escape Games liegen in den Kurs-Repos: `English` (Lost in Sydney),
    `Chemie` (CHIRALITY). Gleiche Domain nitrogen-ai.github.io → download-Attribut
    funktioniert auch dort.
- `downloads/chirality/`: Spielanleitung Digital (PDF, enthält PIN + Codes –
  auf Wunsch des Nutzers öffentlich) und die zwei Pasteur-Kristall-STL.

## Aufbau der Seite (seit 2026-10-17)
- Vier Fachkacheln (`SUBJECTS`) → je Fach ein Kachelgitter (Thumbnails).
- Kachel-Inhalte stehen NICHT mehr als HTML im Dokument, sondern im
  Script-Objekt `ITEMS` (type "app" oder "folder" mit `children`), Texte als
  {en,de}. Statische Seitentexte weiter im `T`-Objekt (data-t).
- Klick → `<dialog id="viewer">` mit Details/Buttons bzw. Ordnerinhalt;
  URL `#open=<id>` (direkt verlinkbar, Zurück schließt).
- Neues Werkzeug = Eintrag in `ITEMS` + id in `SUBJECTS[..].items` oder in
  den `children` eines Ordners. Zählungen werden automatisch berechnet.

## Zusammenspiel
- Beide Buttons pro Karte zeigen auf dieselbe Datei im jeweiligen Repo
  (nitrogen-ai.github.io/training/… bzw. nitrogen-ai.github.io/tools/…):
  "Play Online" öffnet, "Download" lädt herunter (gleiche Domain,
  deshalb funktioniert das download-Attribut).
- Trainer/Werkzeuge NIE hier ablegen oder bearbeiten — immer nur im
  jeweiligen Quell-Repo (`training` bzw. `tools`).
- Neues Werkzeug in `training`/`tools` → hier einen `ITEMS`-Eintrag ergänzen
  (beide Sprachen).

## Konventionen
- Einzelne, offline lauffähige HTML-Datei — keine CDN-Abhängigkeiten.

## Öffentlich — Vorsicht
- Public Repo mit GitHub Pages. Keine personenbezogenen Daten.
