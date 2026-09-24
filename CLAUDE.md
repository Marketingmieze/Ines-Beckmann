# Vault Context

Dieses Vault ist das Zweite Gehirn von Ines.

## Über mich

Ines, Marketing Managerin bei fairbeamtet.de, arbeitet eng mit ihrem Chef Sven Höhne zusammen und verantwortet Website, Artikel und den Aufbau von Social Media. Daneben baut sie mit marketingmieze.com ihr eigenes Marketing-Blog/-Projekt auf. Ausführliches Profil in [[00 Kontext/Über mich.md|00 Kontext/Über mich]].

Ines hat zwei klar getrennte Marken in diesem Vault:
- **fairbeamtet.de** – ihr Arbeitgeber, Versicherungsberatung für Beamte & Co.
- **marketingmieze.com** – ihr eigenes, noch im Aufbau befindliches Projekt

Bei allen inhaltlichen Aufgaben (Content, Texte, Strategie) immer zuerst klären oder aus dem Kontext ableiten, für welche der beiden Marken die Aufgabe ist, und die passenden Kontext-Dateien nutzen.

## Vault-Struktur

- 00 Kontext/: Persönliches Kontext-Profil. `Über mich.md` gilt markenübergreifend. Die Unterordner `Fairbeamtet/` und `Marketingmieze/` enthalten je eigene ICP.md, Angebot.md, Schreibstil.md und Branding.md. Zentrale Referenz für alle inhaltlichen Aufgaben – lies die passenden Dateien, wenn du Content erstellst, Mails schreibst oder Angebote formulierst.
- 01 Inbox/: Schnelle Gedanken, Brain Dumps, unverarbeitete Notizen. Alles was noch keinen festen Platz hat landet hier.
- 02 Projekte/: Aktive Projekte mit konkretem Ziel und Enddatum, getrennt nach `Fairbeamtet/` und `Marketingmieze/`. Projekte starten als einzelne .md-Datei direkt im jeweiligen Marken-Unterordner.
- 03 Bereiche/: Laufende Verantwortungsbereiche ohne Enddatum (aktuell ausschließlich privat: Finanzen, Familie, Pflege Mutter, Gesundheit, Sohn). Jeder Bereich ist ein eigener Ordner mit gleichnamiger Start-Datei, weil Bereiche über die Zeit wachsen.
- 04 Ressourcen/: Referenzmaterial und gesammeltes Wissen (KI, SEO-GEO, Ahrefs, Google Search Console). Jedes Thema ist ein eigener Ordner mit gleichnamiger Start-Datei.
- 05 Daily Notes/: Tägliches Logbuch. Was an einem Tag passiert ist, welche Entscheidungen getroffen wurden, was offen ist. Gibt Kontinuität zwischen Sessions.
- 06 Archiv/: Abgeschlossene Projekte und inaktive Bereiche. Aus dem aktiven Blickfeld, aber durchsuchbar.
- 07 Anhänge/: Bilder, PDFs, Medien. Obsidian legt hier automatisch alle eingefügten Dateien ab.

## Regeln für dieses Vault

- **fairbeamtet.de und marketingmieze.com strikt getrennt halten** – unterschiedliche Zielgruppen, Angebote, Schreibstile und Brandings. Nie vermischen, außer Ines bittet explizit darum.
- Private Bereiche (Finanzen, Familie, Pflege Mutter, Gesundheit, Sohn) enthalten teils sensible/medizinische Informationen. Sorgfältig behandeln, nicht ungefragt mit beruflichen Inhalten vermischen.
- Nutze [[Wikilinks]] für Verknüpfungen zwischen Notizen.
- Neue Notizen ohne klaren Platz kommen in 01 Inbox/.
- Halte Notizen atomar: eine Idee pro Notiz wo möglich. Ausnahme: Daily Notes fassen einen ganzen Tag zusammen.
- Daily Notes benennen im Format: YYYY-MM-DD.md (z. B. 2026-09-23.md). So sortieren sie automatisch chronologisch.
- Nutze YAML Frontmatter: tags, status (aktiv/abgeschlossen/pausiert), erstellt.
- Dateinamen in normaler Schreibweise mit Leerzeichen und Großbuchstaben: Beschreibender Name.md
- Neue Projekte bekommen eine einzelne .md-Datei direkt im passenden Marken-Unterordner unter 02 Projekte/. Einen weiteren Unterordner nur anlegen, wenn ein Projekt tatsächlich mehrere Dateien braucht.
- Bereiche und Ressourcen sind immer Ordner, weil sie über die Zeit wachsen.
- Abgeschlossene Projekte nach 06 Archiv/ verschieben. Nur auf Anweisung von Ines, nicht eigenständig.
- Wenn Dateien erstellt oder verschoben werden, kurz erklären warum.
- Bevor Dateien gelöscht oder überschrieben werden, nachfragen.
- Wenn Ines sagt "merk dir das" oder "speicher das": thematisch richtig einsortieren. Schreibregeln nach der passenden `00 Kontext/[Marke]/Schreibstil.md`, Projekt-Infos in die jeweilige Projekt-Datei, technisches Wissen in 04 Ressourcen/, Vault-Regeln in diese CLAUDE.md. Im Zweifel kurz fragen, wo es hin soll.

## Session-Routinen

### Bei Session-Start

Prüfe 01 Inbox/ auf neue Notizen, zeige was drin liegt, und biete an, die Einträge in die passenden Ordner einzusortieren.

Prüfe außerdem [[03 Bereiche/Termine/Termine.md]] auf anstehende Termine (heute und die nächsten Tage) und nenne sie beim Begrüßen kurz.

### Wenn Ines einen Termin nennt

Termin mit Datum/Uhrzeit in [[03 Bereiche/Termine/Termine.md]] unter "Anstehende Termine" eintragen. Es gibt (noch) keinen echten Kalender-Connector in dieser Session – diese Liste ist der Ersatz, bis das geklärt ist.

### Kontext bei Bedarf

Wenn Ines fragt "Was ist gerade aktuell?", "Wo war ich stehen geblieben?" oder Ähnliches: Lies die letzten 2–3 Daily Notes in 05 Daily Notes/ und die aktiven Projekt-Dateien in 02 Projekte/ (beide Marken-Unterordner) um ein Briefing zu geben.

### Bei Session-Ende

Wenn Ines die Session beendet, "Feierabend" sagt oder ein natürliches Ende erreicht ist:
1. Prüfe [[03 Bereiche/Termine/Termine.md]] auf Termine für den nächsten Tag und erinnere kurz daran.
2. Anbieten:
   - Einen Daily-Note-Eintrag in 05 Daily Notes/ mit einer Zusammenfassung des Tages zu erstellen
   - Neue Erkenntnisse als Notizen zu speichern
   - Die Inbox aufzuräumen, falls nötig

---

## Nach dem Setup

Das Setup ist abgeschlossen. Diese Datei verhält sich ab jetzt als normaler Vault-Kontext.

Falls Ines sagt "Setup nochmal durchführen" oder "Vault neu einrichten", kann bei Bedarf wieder ein Onboarding-Gespräch geführt werden – dann aber auf Basis dieser bestehenden Struktur, nicht bei null anfangen.
