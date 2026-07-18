# Public Changelog

In diesem Dokument werden öffentlich relevante Änderungen an Vnzia zusammengefasst.

Interne Refactorings, Architekturänderungen, Sicherheitsdetails und nicht öffentliche Entwicklungsstände werden hier nicht dokumentiert.

Jeder App-Build bekommt einen eigenen Abschnitt und wird zusätzlich als
[GitHub Release](../../releases) mit dem Tag `build-<nummer>` veröffentlicht.
Wie das abläuft, steht in [RELEASING.md](RELEASING.md).

## Build 119 — 2026-07-18

### Neu

- **Farbschema wählbar:** Hell, Dunkel oder dem System folgend — in den Einstellungen unter „Darstellung".
- **Sprache wählbar:** Deutsch (Standard) und Englisch. Französisch, Spanisch und Italienisch sind bereits sichtbar und folgen in Kürze.

### Verbessert

- Durchgängig deutsche Beschriftungen, unter anderem die Kamera-Abfrage beim Verbinden des Tagebuchs.

## Build 118 — 2026-07-17

### Neu

- **Handbuch:** eine geführte Tour durch alle Funktionen — in der App zum Nachlesen (auch offline) und öffentlich unter [venezia.picturefish.eu/handbuch.html](https://venezia.picturefish.eu/handbuch.html).

## Build 117 — 2026-07-17

### Neu

- **Meine Einreichungen:** eingereichte Feature Requests und Bug Reports bleiben mit ihrer Nummer sichtbar und gleichen sich über iCloud auf deinen Geräten ab.

## Build 116 — 2026-07-17

### Neu

- **Feature vorschlagen** und **Problem melden** direkt aus der App — als öffentliches Issue hier im Repository, ganz ohne GitHub-Konto. Vor dem Senden siehst du genau, was geteilt wird.

## Repository

- Öffentliches Community-Repository für Feature Requests, Bug Reports und Roadmap
- Strukturierte Formulare für Produktfeedback (Feature Request und Bug Report als Issue Forms)
- Vertraulicher Meldeweg für Sicherheitsprobleme über GitHubs „Privately report a security vulnerability"
- Status-, Quellen- und Plattform-Labels für den öffentlichen Triage-Prozess
- Öffentliche Produkt-Roadmap

---

## Format

Künftige Einträge werden nach Version oder Veröffentlichungsdatum gegliedert und in folgende Kategorien eingeordnet:

- **Added** – neue Funktionen
- **Changed** – Änderungen an bestehenden Funktionen
- **Improved** – Verbesserungen der Nutzung oder Performance
- **Fixed** – behobene Fehler
- **Deprecated** – Funktionen, die künftig entfallen sollen
- **Removed** – entfernte Funktionen
- **Security** – allgemein formulierte Sicherheitshinweise ohne ausnutzbare Details