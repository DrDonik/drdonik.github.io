# drdonik.github.io

Startseite unter <https://drdonik.github.io/>. Eine einzelne HTML-Datei ohne
Build-Schritt, ohne Abhängigkeiten, ohne Tracking.

Die Seite verlinkt die Apps, die als Projektseiten in eigenen Repositories
liegen. Sie hostet sie nicht: `https://drdonik.github.io/wetter/` kommt
weiterhin aus `DrDonik/wetter`, nicht aus diesem Repository.

## Pflege

Neue App: eine `<li class="card">` in `index.html` ergänzen, mit Icon,
Titel-Link auf die Projektseite und `Quellcode`-Link auf das Repository. Die
sichtbare Reihenfolge ist die Reihenfolge im Markup.

Die App-Icons liegen als Data-URI in der Datei, damit die Seite eine einzelne
Datei bleibt und nicht bricht, wenn ein Projekt seine Icon-Datei umbenennt. Der
Preis dafür: Ändert eine App ihr Icon, zeigt die Startseite das alte, bis es
hier ersetzt wird. Quelle ist jeweils das `apple-touch-icon` der App, auf
96 × 96 skaliert und für die Anzeige mit 48 × 48 gedacht.

`.nojekyll` schaltet den Jekyll-Build ab. Die Datei liegt hier, damit
GitHub Pages den Inhalt unverändert ausliefert und keine Namenskonventionen
(führender Unterstrich) interpretiert.

## Barrierefreiheit

Ziel ist WCAG 2.2 AA, wie in den anderen Repos.

- Ein Fokusring für die ganze Seite, einmal in `:focus-visible` deklariert.
- Gemessene Kontraste: Fliesstext 6.1:1 hell und 8.4:1 dunkel, Überschriften
  15.2:1 und 15.7:1, Links und Fokusring 8.5:1 und 9.3:1. Die Kartenrahmen
  liegen bei 1.3:1 und 1.5:1 und trennen nur Flächen, sie markieren keine
  Bedienelemente.
- Die App-Icons sind dekorativ (`alt=""`), der Titel daneben nennt die App.
- Die vier gleich lautenden `Quellcode`-Links tragen den App-Namen in einem
  `sr-only`-Span, damit sie sich in der Linkliste unterscheiden.
- `prefers-reduced-motion` schaltet die Hover-Bewegung der Karten ab.

## Lizenz

The Unlicense.
