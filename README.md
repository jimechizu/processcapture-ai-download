# ProcessCapture AI – öffentlicher Download und Website

Dieses öffentliche Verteilungs-Repository ist ausschließlich für die statische Website und freigegebene Windows-Installationsdateien vorgesehen. Es ist **nicht** das Quellcode-Repository der Anwendung. Weder privater Anwendungscode noch interne Dokumentation, Aufnahmen, Zugangsdaten oder Repository-Historie wurden in dieses Website-Paket übernommen.

- Download: https://github.com/jimechizu/processcapture-ai-download/releases/latest
- Website-Version: **0.5.0**, Windows 10 ab Version 2004 / Windows 11, x64.
- Das Installationsprogramm ist nicht digital signiert. Prüfen Sie die SHA256-Prüfsumme vor dem Ausführen. SmartScreen kann „Weitere Informationen → Trotzdem ausführen“ anbieten; das ersetzt keine Prüfung der Datei.
- Die Prüfsumme bezieht sich auf die benannte 0.5.0-Datei, nicht automatisch auf zukünftige Dateien hinter „latest“. Bei jeder neuen Version Website und Prüfsumme gemeinsam aktualisieren.

## Herkunft und Umfang

Ausgangspunkt: Website-Entwurf aus **PR #192** im privaten Ursprungsprojekt (Branch `feature/website`). Dieser Herkunftshinweis veröffentlicht keinen privaten PR-Link oder Anwendungscode und bedeutet nicht, dass der PR übernommen oder geschlossen wurde.

Übernommen wurden ausschließlich `website/` und ausgewählte freigegebene Marken-/Schriftassets. Farben und Sie-Form folgen dem Graphit-/Signalrot-Zielbild. Atkinson Hyperlegible Next wird lokal eingebunden; die SVG-Logos enthalten den Manrope-Schriftzug als Pfade. Vollständige Schriftlizenzen und Markenhinweise: [`licenses/README.md`](licenses/README.md). Eine Lizenz für die private Anwendung wird damit nicht erteilt.

## Dateien und Betrieb

- `index.html`: Landingpage, Download, Prüfsumme, Funktions-/Datenschutzhinweise.
- `impressum.html`, `datenschutz.html`, `legal.css`: Anbieter- und Datenschutzhinweise für GitHub Pages.
- `fonts.css`, `fonts/*.woff2`: lokale Schriftdateien.
- `logo.svg`, `logo-weiss.svg`, `favicon.svg`: Markenassets.
- `licenses/`: vollständige OFL-Texte und Herkunftshinweise.

Kein Build, kein JavaScript, keine externen Schrift-/Skriptressourcen, keine Analyse-Tools und kein lokaler Theme-Speicher. Die Darstellung folgt der Systemeinstellung. PayPal ist nur ein Link und wird erst beim Öffnen aufgerufen. GitHub Pages verarbeitet technisch notwendige Zugriffsdaten einschließlich IP-Adressen für Sicherheitszwecke; Details stehen in der Datenschutzerklärung.

Lokal prüfen: `python3 -m http.server 8080 --bind 127.0.0.1`, dann `http://127.0.0.1:8080` öffnen. Relative Links funktionieren auch unter einem GitHub-Pages-Projektpfad und ohne JavaScript.

## Veröffentlichung und Wartung

1. Den vollständigen öffentlichen Dateiumfang und die freigegebene Installationsdatei unabhängig prüfen.
2. Angezeigte Version, Dateiname und SHA256 gegen die endgültige Installer-Datei und deren Release-Prüfsummendatei vergleichen. Nach einem erneuten Build aktualisieren.
3. Impressum, Datenschutzerklärung und tatsächliche Hosting-/Spendenkonfiguration durch den Anbieter prüfen lassen. Keine verbindliche Rechtsberatung oder rechtliche Zertifizierung.
4. Erst danach gesondert freigegeben veröffentlichen. Die Vorbereitung dieses Pakets führt keinen Push, Merge, Release oder Pages-Deploy aus.

Die beiden Download-Knöpfe verlinken direkt auf die zum angezeigten Versionsstand passende EXE. „Alle Versionen“ führt separat zur öffentlichen Release-Seite. Bei jeder neuen Version müssen EXE-Links, Version und SHA256 gemeinsam aktualisiert werden.

Eine neue Version erfordert die Aktualisierung der Versionsangaben und von `#release-checksum` in `index.html`. Download-Links müssen auf dem öffentlichen Verteilungs-Repository bleiben; keine privaten Ursprungslinks oder internen Dateien ergänzen.

## GitHub Pages und Review

Website: https://jimechizu.github.io/processcapture-ai-download/

Die Erstveröffentlichung nutzt den Branch `feature/public-website` am Root.
Ein Pull Request nach `main` bleibt zur menschlichen Prüfung offen; kein Agent
merged seinen eigenen PR. Nach menschlichem Merge die Pages-Quelle auf `main`
umstellen. Der öffentliche Release-Tag zeigt nur auf die öffentliche
Repository-Historie, niemals auf einen privaten App-Commit.
