# Release-Prozess

Wie aus einem Vnzia-Build eine nachvollziehbare, öffentliche Release-Notiz wird.

## Grundidee: drei Ebenen, eine Build-Nummer

Jede Änderung lässt sich über die **Build-Nummer** durch alle Ebenen verfolgen:

| Ebene | Wo | Für wen | Inhalt |
| --- | --- | --- | --- |
| Technisch | privates Server-Repo (`CHANGELOG.md`, Commits) | Entwicklung | Endpunkte, Migrationen, Tests |
| Öffentlich | dieses Repo: [`CHANGELOG.md`](CHANGELOG.md) + [GitHub Releases](../../releases) | Nutzerinnen und Nutzer | Neu / Verbessert / Behoben |
| Test | TestFlight „What to Test" | Beta-Tester | worauf beim Testen zu achten ist |

Die App-Build-Nummer (`Build 119`), die Server-Version (`v0.22.x`) und der
GitHub-Release-Tag (`build-119`) beschreiben denselben Stand.

## Ablauf je Build

1. **CHANGELOG ergänzen.** In [`CHANGELOG.md`](CHANGELOG.md) einen neuen
   Abschnitt `## Build <N> — <YYYY-MM-DD>` anlegen, mit den passenden
   Kategorien **Neu**, **Verbessert**, **Behoben** (weglassen, was leer ist).
   In Nutzersprache formuliert — keine internen Details, keine Endpunkte.

2. **GitHub Release erstellen.** Aus demselben Text ein Release veröffentlichen:

   ```sh
   gh release create build-<N> \
     --repo sykfar/vnzia-community \
     --title "vnzia Build <N>" \
     --notes-file <notes.md>
   ```

   Der Tag `build-<N>` ist der offizielle, verlinkbare Identifier des Stands.
   Releases sind öffentlich, versioniert und als RSS/Atom abonnierbar
   (`releases.atom`).

3. **TestFlight-Notiz.** Beim Upload eine kurze „What to Test"-Notiz — was neu
   ist und worauf zu achten ist. Bleibt manuell, knapp gehalten.

## Kategorien

- **Neu** — neue Funktionen.
- **Verbessert** — spürbare Verbesserungen an Bestehendem, Performance, Texte.
- **Behoben** — behobene Fehler (allgemein formuliert, ohne ausnutzbare Details).
- **Sicherheit** — nur allgemeine Hinweise; nie Reproduktionswege. Sicherheits­lücken laufen über [SECURITY.md](SECURITY.md), nicht über Releases.

## Was nicht hierher gehört

Interne Refactorings, Architekturentscheidungen, Server-Migrationen,
Dateinamen, private Repository-Links. Diese Notizen beschreiben, **was Nutzer
davon haben** — nicht, wie es intern gebaut ist.
