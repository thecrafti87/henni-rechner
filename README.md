# Henni-Rechner

Ein Längenmaß-Rechner mit der Einheit **Henni** (1 Henni = 1,70 m). Rechnet Längen,
Flächen und Räume um.

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
