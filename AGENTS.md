# Projekt-Regeln (ACCREDO)

Ergänzt die gemeinsamen Regeln aller Projekte (`~/.claude/CLAUDE.md` → `~/ai_dev_workflow_global/rules/RULES.md`, gleiche Abschnittsnummern); bei Widerspruch gilt diese Datei, Sicherheit (§0) hat immer Vorrang. Angelegt am 2026-10-12 aus `~/ai_dev_workflow_global/rules/project_AGENTS.md`.

## 0. Sicherheit
- **Öffentliches Repo und öffentliche Seite** (lu4k87.github.io): keine echten Personendaten, keine internen Dokumente, keine Zugangsdaten; Dokumentauszüge im Prozess sind Beispieltexte.
- Veröffentlichung läuft über den pre-push-Hook (`~/ai_dev_workflow_global/bin/pages_hook.sh`) – nie am Hook vorbei veröffentlichen.

## 4. Projekt-Karte

| Ort | Zweck |
|---|---|
| `index.html` | die ganze Seite (Scrollytelling, Phasen, RACI-Radar, Deliverables-Matrix, Studiengänge; kein Build, kein Server) |
| `data.js` | gemeinsame Daten von `index.html` und `ACCREDO_v2/` (Ablage, Studiengänge, Phasenordner, Dokumenttexte); klassisches Script, damit `file://` geht |
| `README.md` | Funktionen + Ablageorte (Moodle-Kurs „ACCREDO“) |

## 5. Arbeitsweise (Ergänzung)
- **Prüfungen (Definition of Done):** `index.html` direkt im Browser öffnen; hell + dunkel, 360 und 1280 px, Konsole ohne Fehler; Bewegung sanft (Skill `soft-motion`), `prefers-reduced-motion` zeigt den Endzustand.
- **Texte:** Hochschul-Begriffe (SPO, Studiengänge, Gremien) exakt wie in der Seite; neue Texte DE, Zahlen und Namen nur aus belegten Quellen.

## 0c. Skill-Finder
- Allgemeine Skills: Tabelle in `RULES.md` §0c; dieses Projekt hat keine eigenen Skills.

## 5. Arbeitsweise
- **Commit + Push:** direkt in diesem Repo (`git@github.com:lu4k87/__project_accredo.git`), Skill `commit`; Liste aller Projekte: `~/ai_dev_workflow_global/config/projects.yaml`.
- **Agenten** (ohne Nachfrage erlaubt, `RULES.md` §0b): `web-test-runner` (Prüfläufe), `web-ui-verifier` (UI hell + dunkel), `code-explorer` (breite Suche), `security-reviewer` (IT-Sicherheit vor Freigabe ins Netz, Auth, Ports).
