# susertux – Projektübersicht

Öffentliche Übersicht meiner Projekte. Die Arbeits-Repositories sind privat; hier findest du eine Zusammenfassung, was dahinter steckt.

## Über mich

Selfhoster und Hobby-Entwickler aus Deutschland mit Fokus auf ein autonom laufendes Homelab: Proxmox VE als virtualisierte Basis, Home Assistant für die Hausautomation, [Immich](https://pixelunion.eu/) als Foto-Verwaltung (gehostet auf [pixelunion.eu](https://pixelunion.eu/)). Rund um diese Infrastruktur entstehen kleine Python-Tools, die Datenflüsse automatisieren – von GPS-EXIF-Daten bis zum versionskontrollierten Backup. Ergebnisse und learnings landen hier als öffentliche Zusammenfassung.

## Projekte

### [haustein.cc](https://haustein.cc) – Persönliche Website
Zweisprachige (de/en) persönliche Website, gebaut mit Hugo und ausgeliefert über Cloudflare Pages. Highlight ist eine interaktive Leaflet/OpenStreetMap-Karte besuchter Orte, die automatisch aus Fotodaten meiner Immich-Instanz ([pixelunion.eu](https://pixelunion.eu/), GPS-EXIF) generiert wird. Weitere Themen: Home Automation, Aircraft Tracking, technische Infrastruktur. Sicherheits-Fokus: XSS-Schutz, TLS 1.2/1.3 + PQC-Handshake (SSL Labs A+), MDN Observatory A+ (120/100), security.txt, strikte CSP, Service-Worker mit LRU-Tile-Cache. Technische Details transparent im „Technik“-Modal der Seite.

### Immich Places Sync
Automatisierte Synchronisation besuchter Orte aus meiner gehosteten [Immich](https://pixelunion.eu/)-Instanz: GPS-EXIF-Daten werden per Reverse-Geocoding ([Nominatim](https://nominatim.org)/OpenStreetMap) zu Orten aufgelöst und als Datenbasis für die Reise-Karte auf haustein.cc bereitgestellt. Läuft wöchentlich sonntags (04:00 UTC) per GitHub Actions mit Respektierung aller API-Rate-Limits, Geocoding-Cache und robustem Error-Handling – auch Wiederherstellung und Neu-Aufsetzen sind dokumentiert.

### Immich Standort-Tags
Python-Werkzeug zur Verwaltung von Standort-Tags in Immich: Assets ohne Standortinformationen werden automatisch markiert und – nachträglich hinzugefügte GPS-Daten – wieder automatisch getaggt/entfernt. Ein einziger Aufruf für Cleanup und Tagging, mit Unit-Tests (Coverage ~88 %).

### Home Assistant Backup
Versionskontrolliertes Backup der kompletten Home-Assistant-Konfiguration (Automations, Blueprints, Dashboards, Skripte, Sensoren), gepflegt über das Version-Control-Add-on. Änderungen an Automatisierungen sind damit reproduzierbar und über die Git-Historie nachvollziehbar.

### Hardware-Info-Backup
Automatisiertes Backup von Hardware- und Systeminformationen eines Proxmox-VE-Heimservers (Debian 13): LSHW, PCI/USB, CPU-Infos und VM-/Container-Übersicht werden per Skript gesammelt und als Git-Historie archiviert – inklusive Drift-Erkennung bei Hardware-Änderungen. So bleibt dokumentiert, welche Hardware wann ausgetauscht oder erweitert wurde.

### Notizen
Zentrale Ablage für private Notizen, thematisch nach Ordnern gegliedert. Schwerpunkt Reiseplanung: strukturierte Reisepläne, Checklisten (Tickets, Buchungsdaten, Stornofristen) und wiederverwendbare Vorlagen für neue Reisen. Bewusst eigenständig, ohne Querverbindungen zu anderen Repos.

### Wissen & Gedächtnis
Zentrales „Gedächtnis“-Repo für Fakten, Episoden-Protokolle (Session-Tagebücher), strukturierte Daten und Analysen aus laufenden Projekten – als Brücke zwischen den Projekt-Repos, mit klarer Trennung von zeitlosen Fakten und datierten Episoden.

## Schwerpunkte

- Selfhosting & Homelab (Proxmox VE, Home Assistant, Immich)
- Python-Automatisierung rund um Fotodaten und Geocoding
- Statische Websites mit Hugo + Cloudflare Pages
- Git als Backup- und Dokumentationswerkzeug
- Web-Sicherheit: CSP, TLS/PQC, Security-Header-Best-Practices
- OpenStreetMap/Leaflet-Karten mit automatisierten Datenquellen

## Kontakt & Social Profiles

- **Website**: [haustein.cc](https://haustein.cc) – mit Reise-Karte, Technik-Details und Impressum
- **GitHub Pages**: [susertux.github.io](https://susertux.github.io)
- **Mastodon**: [@susertux@norden.social](https://norden.social/@susertux) – verifiziert über `rel="me"` von haustein.cc
- **GitHub**: [@susertux](https://github.com/susertux) – dieses Profil-Repository und Projektübersichten
- **E-Mail**: [github@haustein.cc](mailto:github@haustein.cc) – für Anmerkungen zu Sicherheits- oder Inhaltsfragen

Kein Tracking, keine Newsletter, keine kommerziellen Kanäle. Am schnellsten erreichst du mich über Mastodon oder direkt per E-Mail.
