---
tags: [projekt, fairbeamtet, wettbewerb]
status: aktiv
erstellt: 2026-10-08
start: 2026-10-08
ende: 2026-12-31
---

# Beamtenberater.com

## Ziel

beamtenberater.com als Tier-1-Konkurrenten (siehe [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]]) laufend beobachten: klären, ob der aktuelle Backlink-Anstieg echtes Wachstum oder eine Spam-Welle ist, den tatsächlichen Traffic-Verlauf verfolgen und Content-Lücken bei ihren Top-Seiten für unser eigenes Angebot nutzen. Erster Check-Punkt Ende Q4 2026, danach quartalsweise weiterführen oder abschließen.

## Hintergrund

beamtenberater.com: DR 29, ca. 3.944 Traffic/Monat, 66 gemeinsame Keywords mit fairbeamtet.de (Stand 02.10.2026, siehe [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]]). 8 namentliche Berater, TÜV-Logo, 4,9 Sterne bei 127 Bewertungen auf der Startseite.

Bereits vor diesem Projekt notierte Befunde:
- **28.09.2026** ([[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]]): Ahrefs-Export zeigte Traffic-Einbruch von ~11.529 auf ~3.669 Besuche/Monat (−68 %), teilweise durch URL-Umstellung (Wegfall des abschließenden Slashes) überlagert, aber auch bereinigt ein echter Rückgang.
- **SEO-GEO Status Report** (Abschnitt „Wettbewerbsanalyse: Linkwachstum vs. Ranking-Erfolg"): +153 % Backlinks, +260 % Referring Domains, aber −60 % Top-3-Keywords im 6-Monats-Vergleich – Linkwachstum lief dem Ranking-Erfolg entgegengesetzt.

## Befund vom 08.10.2026 (Live-Ahrefs-Check: Warum die Referring Domains "gestiegen" sind)

Der in Ahrefs sichtbare Anstieg der verweisenden Domains – von 487 (August 2026) auf 968 (Oktober 2026), fast eine Verdopplung in gut einem Monat – ist **keine echte Linkbuilding-Kampagne, sondern eine Spam-Link-Welle**:

- Über 50 der neuen verweisenden Domains wurden am **28./29.09.2026** innerhalb weniger Stunden neu registriert, fast ausschließlich `.shop`-Domains mit generischen SEO-Buzzword-Namen (z. B. `sharpboosthub.shop`, `smartranklab.shop`, `ranklora.shop`, `crispboosthub.shop`, `indexxaro.shop`, `rankzaro.shop`, `seoqira.shop` …).
- Alle diese Domains haben **Domain Rating 0**, sind von Ahrefs explizit als **`is_spam: true`** markiert, liefern je genau **1 Link** und haben **0 geschätzten eigenen Traffic**.
- Einzige Ausnahme unter den neuesten Links: `gadmo.eu` (DR 49, 3.478 eigener Traffic, seit 01.10.2026) – ein einzelner legitimer neuer Verweis, der Rest ist der Spam-Block.
- Trotz der fast verdoppelten Referring-Domains-Zahl ist die **Domain Rating nicht gestiegen**: Peak 31 im Januar 2026, aktuell 29 (Oktober 2026) – Ahrefs gewichtet Spam-Domains in der DR-Berechnung kaum, was den Verdacht bestätigt.
- Der **tatsächliche organische Traffic** (Ländefilter DE) ist im gleichen Zeitraum weiter gefallen statt gestiegen: von einem Hoch von ~11.509 Besuchen/Monat (August 2025) auf nur noch **~2.872/Monat** (Oktober 2026) – ein Rückgang von rund **75 % seit dem Peak**, mit einem Tiefpunkt von ~1.649 im August 2026.

**Einordnung:** Das bestätigt zum wiederholten Mal (siehe auch die Fälle beamtenservice und alexander-kuhlen.de in [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]]) das Muster: Wettbewerber, die im Ranking abstürzen, bauen danach Massen-Spam-Links auf – ohne messbare Wirkung auf Rankings oder Domain Rating. Der scheinbare „Anstieg" bei beamtenberater.com ist also eher ein Alarmsignal für den Wettbewerber als ein Erfolg – möglicherweise eine gekaufte, wirkungslose „SEO-Rettungsmaßnahme", im Zweifel sogar ein Hinweis auf eine kompromittierte/gehackte Domain, die fremd als Linkfarm-Ziel genutzt wird (auffällig viele frisch registrierte, thematisch unpassende `.shop`-Domains mit exakt 1 Link). Das ist eine Vermutung, keine Bestätigung – nicht weiter verfolgt, da es für uns ohnehin keine Handlungsrelevanz hat.

## Nachtrag vom 08.10.2026: Warum beamtenberater im Vergleich zu allen Wettbewerbern "gestiegen" ist

Ines' Beobachtung stimmt: Im direkten Aug.→Okt. 2026-Vergleich (DE, Ahrefs) ist beamtenberater.com die einzige Domain unter den geprüften Tier-1-Konkurrenten (und auch im Vergleich zu uns selbst), die im Traffic gestiegen ist, während alle anderen fielen:

| Domain | Aug. 2026 | Okt. 2026 | Veränderung |
|---|---|---|---|
| **beamtenberater.com** | 1.649 | 2.872 | **+74 %** |
| beamtenservice.de | 4.698 | 2.390 | −49 % |
| info-beihilfe.de | 8.179 | 4.390 | −46 % |
| beamten-infoportal.de | 7.738 | 4.001 | −48 % |
| schlemann.com | 4.099 | 4.155 | ±0 % |
| fairbeamtet.de (wir) | 2.338 | 1.117 | −52 % |

**Grund 1 – es ist eine Erholung vom eigenen Fehler, kein echtes Wachstum über das alte Niveau hinaus:** Top-Pages-Vergleich 01.08. vs. 01.10.2026 zeigt für praktisch jede aktuelle Top-Seite ein 1:1-Gegenstück mit identischer URL, nur mit abschließendem Slash (z. B. `/kindergeld-beamte/` → `/kindergeld-beamte`, `/freie-heilfuersorge/` → `/freie-heilfuersorge`, `/familienzuschlag-beamte/` → `/familienzuschlag-beamte`). Das ist eine URL-Migration (Wegfall des abschließenden Slashes), die in Ahrefs vorübergehend wie Traffic-Verlust + Neugewinn aussieht. Der Tiefpunkt (1.649, August 2026) ist der Migrations-Einbruch, die Erholung auf 2.872 (Oktober) ist die Rückübertragung der Rankings auf die neuen URLs – **kein** Wachstum über das Vor-Krise-Niveau hinaus: 2.872 liegt immer noch 31 % unter dem März-2026-Wert (4.180) und 75 % unter dem Allzeithoch (11.509, August 2025).

**Grund 2 – die Spam-Backlinks (oben) sind nachweislich nicht die Ursache:** Domain Rating blieb während der gesamten Erholungsphase flach bis leicht fallend (30 im Juli/August → 29 im Oktober), trotz der Spam-Welle vom 28./29.09. Zeitliche Überlappung, aber kein Kausalzusammenhang.

**Grund 3 – der Rest der Nische (inkl. uns) fällt im selben Fenster unabhängig weiter:** Fast jedes geprüfte Keyword von beamtenberater zeigt inzwischen das SERP-Feature `ai_overview` – AI Overviews sind in der Beamten-Nische seit Sommer 2026 flächendeckend präsent und drücken vermutlich bei allen Domains die Klicks, unabhängig vom Verhalten einzelner Wettbewerber. Die zwei Linien – „beamtenberater erholt sich von der eigenen Migration" und „der Rest der Nische sinkt weiter (vermutlich AI-Overview-bedingt)" – kreuzen sich rein zufällig in diesem Zeitraum. Das erzeugt den Eindruck eines Wettbewerbsvorteils, ist aber keiner.

**Einordnung für uns:** Kein Grund zur Sorge wegen beamtenberater – aber der eigene Rückgang (fairbeamtet −52 % seit August 2026) ist größer als der von beamtenberater und sollte eigenständig priorisiert untersucht werden (siehe [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Los-Schmerz-Wochos.md|Los-Schmerz-Wochos]]).

## Top-Seiten (Stand 08.10.2026, Ländefilter DE)

| URL | Traffic/Monat | Top-Keyword | Position |
|---|---|---|---|
| /kindergeld-beamte | 827 | kindergeld beamte | 2 |
| /beihilfe/berlin/bearbeitungsstand | 336 | bearbeitungsstand beihilfe berlin | 4 |
| /was-bekommt-ein-beamter-bei-dienstunfaehigkeit | 217 | dienstunfähigkeit beamte | 2 |
| /beihilfe/schleswig-holstein/bearbeitungsstand | 188 | bearbeitungsstand beihilfe sh | 1 |
| /beamter-auf-lebenszeit | 155 | beamter auf lebenszeit | 5 |
| /beamter-auf-widerruf | 117 | beamter auf widerruf | 7 |
| /wie-sind-beamte-krankenversichert | 106 | zahlen beamte in die krankenkasse ein | 5 |
| /heilfuersorge-nrw | 99 | freie heilfürsorge nrw | 6 |
| /wie-teuer-ist-die-krankenversicherung-fuer-beamte | 99 | beamter krankenversicherung kosten | 6 |
| /beihilfe/hessen/bearbeitungsstand | 89 | bearbeitungsstand beihilfe hessen | 6 |

Auffällig: Mehrere der stärksten Seiten sind „Bearbeitungsstand Beihilfe [Bundesland]"-Seiten (Berlin, Schleswig-Holstein, Hessen, NRW) – ein ähnliches Muster wie die „Beihilfe [Bundesland]"-Lücke, die am 02.10.2026 bereits bei beamtenservice als Content-Chance für uns notiert wurde (siehe [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]]).

## Nächste Schritte

- [ ] Monatlich gegenchecken, ob sich der Traffic-Rückgang stabilisiert oder weiter fällt (gleicher Turnus wie [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Los-Schmerz-Wochos.md|Los-Schmerz-Wochos]])
- [ ] Beobachten, ob die Spam-Linkwelle weitergeht oder ein Einzelereignis war
- [ ] Prüfen, ob „Bearbeitungsstand Beihilfe [Bundesland]"-Seiten eine eigene Content-Chance sind (Überschneidung mit der bereits notierten „Beihilfe pro Bundesland"-Lücke bei beamtenservice klären, evtl. zusammenlegen)
- [ ] Entscheiden, ob dieses Projekt Ende Q4 2026 abgeschlossen oder weitergeführt wird
- [ ] Wichtiger als beamtenberater: eigenen Traffic-Rückgang (−52 % seit August 2026) untersuchen – ist das bei uns auch eine technische Ursache (Migration, Indexierung) oder reiner AI-Overview-Effekt? An [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Los-Schmerz-Wochos.md|Los-Schmerz-Wochos]] zurückspielen
- [ ] Verifizieren, ob AI Overviews tatsächlich flächendeckend neu in der Beamten-Nische sind (z. B. via Brand Radar/SEOgets), statt nur aus den SERP-Features der Ahrefs-Stichprobe zu schließen

## Notizen

Rohdaten per Ahrefs API (Site Explorer, Ländefilter DE wo zutreffend) live gezogen am 08.10.2026.
