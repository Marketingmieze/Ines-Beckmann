---
tags: [projekt, fairbeamtet, priorität-hoch]
status: aktiv
erstellt: 2026-09-30
start: 2026-09-30
ende: 2027-12-31
---

# Los-Schmerz-Wochos

## Ziel

Bis Ende 2027 bei Google- und GEO-Sichtbarkeit an Beamtenservice.de vorbeiziehen und die Führung übernehmen.

Das ist unser Herzprojekt mit der höchsten Priorität. Der ganze Analyse-Aufwand (Ahrefs, SEOgets, Content-Vergleich) läuft hier zusammen, um genau dieses Ziel zu erreichen.

## Hintergrund

Hauptwettbewerber: **Beamtenservice.de** ([https://beamtenservice.de/](https://beamtenservice.de/)), betrieben von Shahryar Honarbakhsh ("Shary") – eigentlich Freund und Kollege.

Shary war auf unserer Weihnachtsfeier, hat sich erzählen lassen, was bei uns gut funktioniert, und danach gezielt unsere besten Seiten kopiert – u. a. die DBV-vs.-Debeka-Seite – sowie weitere Inhalte übernommen, wo es ging. Da er unsere Seite trackt und misst, wird er merken, wenn wir ihn überholen – das ist Teil der Botschaft.

Der Projektname ist Programm: Wir wollen ihm mit besseren Zahlen den Stinkefinger zeigen – nicht durch Kopieren, sondern indem wir es besser machen als er.

## Status

In Bearbeitung – Setup-Phase, weitere Infos und Analysen folgen.

## Umsetzungsplan

Sven hat einen detaillierten 13-Wochen-Umsetzungsplan ausgearbeitet (509 Stunden, Stand 30.09.2026): [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Content-Plan.md|Content-Plan]]. Er deckt Woche 1 bis 13 ab (Messbarkeit & Quick Fixes → Vergleichsseite → Snippets/Redaktionsleitlinie → verlorene PKV-Seiten → Kostenseite → Transaktionsseiten → Themenlücken → DU-Seiten → eigene Bestandsdaten → Hygiene) plus eine Parallelspur (Fachpressen-Reputation, Markenbekanntheit, monatliche Messung). Das ist aktuell unsere konkrete Aufgabenliste für die nächsten Wochen.

## Nächste Schritte

- [ ] Umsetzung des [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Content-Plan.md|Content-Plans]] mit Woche 1 starten (Brand Radar, GA4 Key Event, Rank Tracker – siehe dort)
- [ ] Mit Sven klären: Claude als Datenquelle im Ahrefs Brand Radar Report einschalten (aktuell „off", wie Grok) – Entscheidung liegt bei ihm, nicht eigenständig umgestellt. Prompts dafür liegen schon fertig in [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Brand Radar Prompts.md|Brand Radar Prompts]].
- [ ] Mit Sven klären: „AggregateRating und FAQPage entfernen" (Woche 1) – auf fairbeamtet.de laufen gleichzeitig **Rank Math** und **Schema Pro**, beide können Schema-Markup ausspielen. AggregateRating bestätigt auf `/private-krankenversicherung/beamte/` gefunden (per Live-Check des Seitenquellcodes am 05.10.2026). Bevor da jemand an den Plugin-Einstellungen schraubt, muss Sven entscheiden, welches Plugin die „Quelle der Wahrheit" ist – sonst überschreibt eins das andere.
- [ ] Mit Sven klären: Fehlender Autor auf `/pkv-ratgeber/pkv-vergleich-beamte/` (Woche 1, Teil der Vergleichsseiten-Fixes) – die Seite läuft über ein Elementor-Theme-Builder-Template. Zwei mögliche Ursachen: (1) der native WP-Autor ist am Beitrag selbst nicht gesetzt, (2) das Theme-Builder-Template zeigt gar kein Autor-Widget an. Eine Template-Änderung wirkt sich vermutlich auf mehrere Ratgeber-Seiten gleichzeitig aus – deshalb bewusst Svens Entscheidung, nicht eigenständig am gemeinsamen Template geändert.
- [ ] Gegenchecken, ob die ursprünglich für Beamtenservice.de notierten Referring-Domains-Werte (774/668) evtl. eine Verwechslung mit fairbeamtet.de waren – siehe Hinweis in [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Messungen/2026-09.md|Messung 2026-09]]
- [ ] Kopierte/übernommene Seiten (z. B. DBV vs. Debeka) identifizieren und Differenzierungsstrategie festlegen
- [ ] Konkrete Meilensteine bis 31.12.2027 definieren

## Wettbewerber

- **Beamtenservice.de** – [https://beamtenservice.de/](https://beamtenservice.de/), Betreiber: Shahryar Honarbakhsh ("Shary")

Siehe auch die laufende, marktweite Konkurrenzbeobachtung in [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]], wo beamtenservice bereits als einer der bekannten Wettbewerber geführt wird.

## Fortschrittsmessung

**Turnus:** monatlich messen, quartalsweise entscheiden. Begründung: Der Relaunch wirkte nach 6–10 Wochen, die Vorerkrankungsseiten brauchten 56 Tage bis zum Nachweis – eine Wochenmessung zeigt nur Schwankungen, die man für Trends hält, und Maßnahmen würden abgebrochen, bevor sie greifen. Bei 15 Monaten Laufzeit bis 31.12.2027 ergibt das 15 Messpunkte – genug für eine Kurve, zu wenig für Aktionismus.

**Leitzahl:** Unser Anteil am gemeinsamen Traffic-Wert (uns vs. Beamtenservice.de). Muss über 50 % steigen, dann haben wir überholt. Anders als ein reiner Faktor bewegt sich der Anteil auch dann, wenn beide gleichzeitig verlieren – und das tun aktuell beide.

Jede Messung ist eine eigene Datei nach dem Muster `YYYY-MM.md` in [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Messungen/|Messungen]] (eine Zeile/Datei je Monat). Überblick über alle Monate: [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Fortschritt.base|Fortschritt.base]] mit fünf Ansichten (Der Abstand, Traffic-Wert und Traffic, Keywords nach Position, Unsere eigenen Zahlen, Links und Autorität).

Baseline (live per Ahrefs/SEOgets gezogen): [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Messungen/2026-09.md|Messung 2026-09]] – Stand 30.09.2026: Anteil 15,0 %, Abstand Traffic-Wert 5,66×, Rückstand Platz-1-Keywords 85, Rückstand Top-3-Keywords 158, Abstand Traffic 2,18×. (Rückstand Platz-1 deckt sich exakt mit der ursprünglichen Schätzung, die anderen Werte wurden leicht korrigiert – Details in der Messnotiz.)

Methodik-Fixpunkte für vergleichbare Monate (Details siehe Baseline-Notiz): Keyword-Bänder immer mit Länderfilter DE, verweisende Domains immer mit Modus-Angabe (subdomains/domain), GSC-Zeitraum immer 28 Tage.

Die Base zeigt bewusst auch, was (noch) nicht gemessen wird (Spalte „Messsystem"): KI Share of Voice, Beratungsanfragen und Geld-Keyword-Abdeckung sind aktuell Lücken – lieber sichtbar unvollständig als scheinbar vollständig.

Allgemeine, marktweite Konkurrenzbeobachtung (auch andere Wettbewerber) bleibt in [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]].

## Notizen

- [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Marken-Kannibalisierung.md|Marken-Kannibalisierung]] (05.10.2026): GSC-Analyse zur Woche-1-Aufgabe – Team-Seite und Tipps-Artikel ranken im Schnitt sogar vor der Startseite für „fairbeamtet", HTTP-Duplikat ohne Weiterleitung bestätigt.

