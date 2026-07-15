# ClassroomSpark

## Was das ist
- Landingpage für Lehrkräfte, die die interaktiven Trainer vorstellt.
- Besteht nur aus index.html. Die Trainer selbst liegen im Repo `training`.

## Zusammenspiel
- Beide Buttons pro Trainer zeigen auf nitrogen-ai.github.io/training/:
  "Play Online" öffnet, "Download" lädt herunter (gleiche Domain,
  deshalb funktioniert das download-Attribut).
- Trainer NIE hier ablegen oder bearbeiten — immer nur in `training`.
- Neuer Trainer in `training` → hier eine Karte in index.html ergänzen.

## Konventionen
- Einzelne, offline lauffähige HTML-Datei — keine CDN-Abhängigkeiten.

## Öffentlich — Vorsicht
- Public Repo mit GitHub Pages. Keine personenbezogenen Daten.
