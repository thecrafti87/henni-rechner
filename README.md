# Henni-Rechner

Ein Längenmaß-Rechner mit der Einheit **Henni**. Rechnet Längen, Flächen und Räume um.

## Was ein Henni ist

Der Henni ist **keine Naturkonstante**. Wie jedes Längennormal gilt er nur unter
festgelegten Bedingungen — das Urmeter galt aus demselben Grund nur bei 0 °C.

| | |
| --- | --- |
| **Nennwert** | 1 Henni = 1,700 m |
| **Bezugsbedingungen** | Arbeitszustand, 21 °C |

Zwei Größen verändern ihn:

- **Zustand.** Der *Roh-Henni* ist der Körper selbst (1,670 m). Der *Arbeits-Henni* ist
  derselbe Körper in Arbeitsschuhen; die Differenz ist die Sohle mit 30 mm. Der
  veröffentlichte Wert 1,70 m ist der Arbeits-Henni, deshalb ist er der Vorgabezustand.
- **Temperatur.** Körper und Sohle dehnen sich unterschiedlich stark und werden deshalb
  getrennt gerechnet: Gewebe mit 6,9 × 10⁻⁵ /K (lineare Ausdehnung von Wasser), Gummi mit
  2,0 × 10⁻⁴ /K. Über die einstellbare Spanne von −10 bis 45 °C bewegt sich der Henni um
  knapp sieben Millimeter.

Sichtbar wird das nicht am Ergebnis in Hennis — dort steckt es in den hinteren
Nachkommastellen —, sondern am ausgewiesenen Wert der Einheit selbst, in Millimetern und
ppm. Genau so klein sind die Effekte, um die es in der Längenmesstechnik geht.

Die 30 mm Sohlenhöhe sind ein üblicher Wert für Sicherheitsschuhe, kein gemessener. Wer
nachmisst, ändert `SOHLE_M` in `index.html` — alles andere folgt daraus.

Läuft unter **https://henni-rechner.de**

## Aufbau

Eine einzelne, in sich geschlossene HTML-Datei plus drei Bilder. Kein Build, kein
Server, keine Abhängigkeiten außer Google Fonts. Wer etwas ändern will, öffnet
`index.html` — das ist alles.

| Datei | Wofür |
| --- | --- |
| `index.html` | die ganze Anwendung: Auszeichnung, Gestaltung, Rechenlogik |
| `og.png` | Vorschaubild für geteilte Links |
| `favicon.png`, `apple-touch-icon.png` | Symbole für Browser-Tab und Startbildschirm |
| `CNAME` | die Domain, unter der GitHub Pages ausliefert |

## Veröffentlichen

Ein Push auf `main` genügt — GitHub Pages liefert den Stand der Wurzel aus.

```bash
git add -A && git commit -m "..." && git push
```

Die Domain gehört einem Kollegen; ihr DNS liegt weiterhin bei Strato und zeigt über
vier A-Records auf GitHub. An den Mail-Einträgen der Domain wurde nichts geändert.
Wird `CNAME` gelöscht, fällt die Seite auf die `github.io`-Adresse zurück.
