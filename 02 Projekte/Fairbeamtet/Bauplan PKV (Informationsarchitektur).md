---
tags:
  - projekt
  - fairbeamtet
status: aktiv
erstellt: 2026-10-29
quelle:
  - "07 Anhänge/Bauplan PKV fairbeamtet.de 2026-10-24.pdf"
  - "07 Anhänge/Strukturbaum PKV fairbeamtet.de - Fassung 2 2026-10-24.pdf"
---

# Bauplan PKV (Informationsarchitektur)

Der verbindliche Soll-Zustand für den gesamten `/pkv/`-Bereich von fairbeamtet.de: welche Seiten es geben soll, wie sie zueinander stehen, und wo jeder bestehende Artikel hinzieht. Basis für alle künftigen PKV-Ratgeber und für die Umstrukturierung bestehender Inhalte. Stand der Keyword-Map: 23.10.2026.

**Fassung 2** ist nach Best Practices überarbeitet: **114 Seiten statt 442** in der ersten Fassung — deutlich schlanker.

## Ziel

Ordnung statt Wildwuchs: eine klare Eltern/Kind-Struktur, höchstens drei URL-Ebenen, jede Seite ab 50 Suchen/Monat eigenständig, alles darunter als Abschnitt eingeordnet statt als eigene dünne Seite.

**URL-Regel:** `/pkv/ › [Anbieter] › [Thema] › [Unterthema] › [Zielgruppe]` — jede Ebene optional, Reihenfolge fest. Ausnahme Beitragserhöhung: `Thema › Jahr › Anbieter`.

## Navigation (7 Menüpunkte + Button)

Das Menü selbst ist keine URL-Ebene.

- **Beratung** (Button) · `/pkv/beratung/`
- **Einstieg** — PKV für Beamte, Voraussetzungen, PKV oder GKV, Anwartschaft und Optionstarif
- **Für wen** — Beamtenanwärter, Referendare, Lehrer, Polizei, Pensionäre, Familie und Kinder
- **Kosten** — Kosten, Beitragserhöhung, Beitragsrückerstattung
- **Vergleich und Anbieter** — Vergleich und Test, Anbieter, Erfahrungen
- **Gesundheitsprüfung** — Gesundheitsprüfung und Vorerkrankungen, Öffnungsaktion
- **Leistungen und Tarife** — Leistungen, Tarife, Pflegepflichtversicherung, Zusatzversicherung, Krankentagegeld, Ausland, Abrechnung und Service
- **Wechsel und Alter** — Wechsel, Tarifwechsel, Basistarif und Sozialtarife, PKV im Alter

## Die neun Themenwelten (`/pkv/`-Pillar, 546.110 Suchen/Monat)

| Themenwelt | Seiten | Suchvolumen (inkl. Unterseiten) |
|---|---|---|
| Einstieg für Beamte | 16 Seiten · 9 bestehende | Voraussetzungen 21.090 · PKV oder GKV 17.740 · Beamte 9.230 · Anwartschaft/Optionstarif 3.050 · Beamtenanwärter 1.470 · Referendare 1.200 · Lehrer 630 · Polizei 310 |
| Kosten und Beiträge | 33 Seiten · 12 bestehende | Kosten 45.870 · Beitragserhöhung 3.140 · Beitragsrückerstattung 460 |
| Vergleich und Beratung | 26 Seiten · 12 bestehende | Vergleich und Test 30.880 · Abschluss und Beratung 3.650 · Erfahrungen 180 |
| Gesundheitsprüfung und Öffnungsaktion | 6 Seiten · 8 bestehende | Gesundheitsprüfung/Vorerkrankungen 4.440 · Öffnungsaktion 2.160 |
| Leistungen und Tarife | 22 Seiten · 6 bestehende | Zusatzversicherung 56.370 · Pflegepflichtversicherung 3.080 · Krankentagegeld 2.420 · Leistungen 2.110 · Abrechnung/Service 1.280 · Tarife 1.220 · Ausland 610 |
| Wechsel und Tarifwechsel | 25 Seiten · 0 bestehende | Wechsel 21.240 · Basistarif/Sozialtarife 9.590 · Tarifwechsel 1.930 |
| Familie und Alter | 13 Seiten · 3 bestehende | PKV im Alter 9.460 · Familie und Kinder 4.290 · Pensionäre 380 |
| Andere Zielgruppen | 7 Seiten · 0 bestehende | Rentner, Studenten, Selbstständige, Angestellte, Arbeitslose, Privatiers, Ärzte |
| Anbieter | 293 Seiten · 6 bestehende | Debeka 37.700 · DKV 32.490 · Barmenia 23.970 · DBV 23.480 · Allianz 9.870 · HUK-Coburg 9.450 · HanseMerkur 9.060 · AXA 8.360 · Signal Iduna 5.310 · Hallesche 3.690 · ARAG 3.640 · DEVK 3.150 · und 26 weitere |

**Anbieter-Hubs** hängen direkt unter `/pkv/` (z. B. `/pkv/debeka/`). Die Übersicht `/pkv/anbieter/` verlinkt alle, ist aber nicht ihre Elternseite.

**Beiträge:** nur datierte Anlässe, Kategorie „PKV aktuell". Aktuell nur ein Beitrag mit Keyword-Daten: Zukunft der PKV (`/pkv-zukunft/`).

**Nicht Teil dieses Plans:** Beihilfe und BU/DU bekommen je eine eigene Struktur.

## Seiten-Typen in Fassung 2

- **1 · Eltern/Kind-Struktur** — 14 Eltern-Seiten, 60 Kind-Seiten. Höchstens drei Ebenen (`/pkv/ › Thema › Unterthema`), einzige Ausnahme das Jahresarchiv der Beitragserhöhungen.
- **2 · Kategorien und Beiträge** — aktuell keine. „PKV aktuell" entsteht erst, wenn mehrere datierte Anlässe zusammenkommen.
- **3 · Einzel-Seiten** — 53 Seiten ohne Kind-Seiten, direkt unter `/pkv/` (Themen, Zielgruppen, kleinere Anbieter).
- **4 · Einzel-Beiträge** — 1: Zukunft der PKV.

## Wie bestehende Inhalte einsortiert werden

Jede bestehende Seite/jeder Beitrag ist im Bauplan einem von fünf Zuständen zugeordnet:

- **UMZIEHEN** — Inhalt bleibt, zieht auf die neue URL im Bauplan
- **ZUSAMMENLEGEN** — mehrere bestehende Inhalte werden zu einer Seite verschmolzen (z. B. 4 Artikel zu „Günstige PKV" → eine Seite; 5 Artikel zu „Abschluss und Beratung" → eine Seite)
- **ALS ABSCHNITT** — wird Teil einer größeren Seite statt eigener URL
- **BLEIBT BEITRAG** — bleibt als datierter Einzelbeitrag bestehen (z. B. „Testsieger private Krankenversicherung 2019")
- **EINORDNEN** — wird in eine bestehende Themenseite einsortiert (betrifft vor allem die Vorerkrankungs-Artikel: Brustimplantate, Asthma, Corona, Hashimoto, Heuschnupfen, Migräne, Übergewicht → alle unter Gesundheitsprüfung/Vorerkrankungen)

Die vollständige Zuordnung jeder einzelnen bestehenden Seite steht im PDF [[07 Anhänge/Bauplan PKV fairbeamtet.de 2026-10-24.pdf]] (Seite für Seite je Themenwelt) und im Strukturbaum [[07 Anhänge/Strukturbaum PKV fairbeamtet.de - Fassung 2 2026-10-24.pdf]] (vollständige URL-Liste).

## Warum das für den Content wichtig ist

Jeder neue PKV-Ratgeber und jede Überarbeitung einer bestehenden Seite richtet sich ab jetzt nach diesem Bauplan: welche URL, welche Eltern-Seite, ob Einzel-Seite oder Teil eines größeren Themas. Das verhindert, dass [[Content Creatorin Claudia]] oder die Wochenplanung aus [[Content-Plan|Content-Plan (Los-Schmerz-Wochos)]] neue Seiten anlegt, die dem Zielzustand widersprechen.

## Referenzen

- [[02 Projekte/Fairbeamtet/Content-Erstellung.md|Content-Erstellung]] — das übergeordnete Projekt, in dem neue Artikel entstehen
- [[Content-Plan|Content-Plan (Los-Schmerz-Wochos)]] — Wochenplan mit konkreten Content-Aufgaben, u. a. Themenlücken im PKV-Bereich
- [[04 Ressourcen/Googles No. 1/Interne Verlinkung und Informationsarchitektur.md|Interne Verlinkung und Informationsarchitektur]] — das SEO-Grundlagenwissen, auf dem dieser Bauplan aufbaut
- [[04 Ressourcen/PKV und Beihilfe/PKV und Beihilfe.md|PKV und Beihilfe]] — das Fachwissen zu den Themen, die hier strukturiert werden
- [[Content Creatorin Claudia]] — nutzt diesen Bauplan bei der Themenplanung für neue Ratgeber
