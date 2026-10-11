# EA 5: Kamerabewegung

Einsendeaufgabe 5, Modul Graphical Visualisation Technologies, TH Lübeck, Wintersemester 2026/27.

Eine einseitige WebGL-Anwendung (rohes WebGL 1, kein Framework) mit einer Szene aus
Kugel, Torus, Zylinder, Kegel und Quader auf einer Bodenplatte. Die Kamera kreist über
die Pfeiltasten auf einer Kreisbahn um die Y-Achse (View-Matrix mit `lookAt`). Die Kugel
in der Mitte ist ein rekursives Kugelmodell (Oktaeder als Seed, Dreiecksteilung), dessen
Rekursionstiefe mit zwei Buttons einstellbar ist.

## Live-Demo

Öffentlich erreichbar unter:
<https://merganh.github.io/gvt-ea5-kamerabewegung/>

## Lokal ausführen

Kein Build-Schritt. Die Seite lässt sich über einen lokalen Server öffnen:

```bash
python3 -m http.server 8000
# dann im Browser: http://localhost:8000
```

## Deployment via GitHub Pages

Im Repo liegt ein Workflow unter `.github/workflows/pages.yml`, der die Seite bei
jedem Push auf `main` automatisch nach GitHub Pages deployt. Einmalig im Repo
unter **Settings → Pages → Build and deployment → Source** `GitHub Actions`
wählen.

## Aufbau

- `index.html`: gesamte Anwendung in einer Datei (HTML, CSS, JS inline)

Es werden keine externen Bibliotheken oder Bilder verwendet.

## Bedienung

- **Pfeil links / rechts**: Kamera kreist um die Szene (Gedrückthalten wiederholt)
- **N**: Radius der Kreisbahn vergrößern
- **Shift+N**: Radius der Kreisbahn verkleinern
- **Buttons + Tiefe / − Tiefe**: Rekursionstiefe der Kugel (0 bis 7, ab 7 mit `OES_element_index_uint`)

## Quelltext-Markierung

Die für die Aufgabe geschriebenen JavaScript-Stellen sind mit
`// START EA5_KAMERABEWEGUNG` und `// END EA5_KAMERABEWEGUNG` markiert.
