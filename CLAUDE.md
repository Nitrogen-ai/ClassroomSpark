# ClassroomSpark

## Was das ist
- Landingpage für Lehrkräfte, die die interaktiven Trainer und
  fachübergreifenden Werkzeuge vorstellt.
- Besteht nur aus index.html. Die Werkzeuge selbst liegen in zwei Repos:
  - `training` — fachspezifische Trainer (Kategorien "English"/"Chemistry").
  - `tools` — fachübergreifende Werkzeuge (Kategorie "General Tools" /
    "Allgemeine Werkzeuge"), z. B. das Sitzplan-Werkzeug.

## Zusammenspiel
- Beide Buttons pro Karte zeigen auf dieselbe Datei im jeweiligen Repo
  (nitrogen-ai.github.io/training/… bzw. nitrogen-ai.github.io/tools/…):
  "Play Online" öffnet, "Download" lädt herunter (gleiche Domain,
  deshalb funktioniert das download-Attribut).
- Trainer/Werkzeuge NIE hier ablegen oder bearbeiten — immer nur im
  jeweiligen Quell-Repo (`training` bzw. `tools`).
- Neues Werkzeug in `training`/`tools` → hier eine Karte in index.html
  ergänzen (inkl. beider Sprachversionen im `T`-Objekt im Script).

## Konventionen
- Einzelne, offline lauffähige HTML-Datei — keine CDN-Abhängigkeiten.

## Öffentlich — Vorsicht
- Public Repo mit GitHub Pages. Keine personenbezogenen Daten.
