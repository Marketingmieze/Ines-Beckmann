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

## Site-Audit-Crawl vom 08.10.2026 (Ahrefs Site Audit, 440 gecrawlte URLs)

Erster vollständiger technischer Crawl von beamtenberater.com (Ahrefs-Projekt „Beamtenberater", ID 10501118, abgeschlossen 08.10.2026). **Health Score: 81/100** – 84 Error-, 204 Warning- und 334 Notice-Befunde von insgesamt 440 gecrawlten URLs. Zum Vergleich: unser eigenes Site-Audit-Projekt „Fairbeamtet" (954 URLs) liegt aktuell bei Health Score 99 mit nur 5 Errors.

Auffälligste Befunde bei beamtenberater:

1. **76 verwaiste Seiten** (Error, „Orphan page" – keine eingehenden internen Links). Auffällig: Das betrifft überproportional ihre Longtail-/Nischenseiten, u. a. mehrere Bundesland-spezifische Seiten (`dienstunfaehigkeit-beamte-schleswig-holstein`, `-bayern`, `-baden-wuerttemberg`; `heilfuersorge-saarland`, `heilfuersorge-rheinland-pfalz`) sowie Versicherer-Vergleichsseiten (`beitragsgarantie-dbv`, `-concordia`, `-barmenia`) und weitere Themenseiten (`unser-team`, `rechtsschutzversicherung`, `krankentagegeld`, `kuendigungsfrist-pkv` u. a.). Diese Seiten existieren und sind indexierbar, aber ohne interne Verlinkung für Google schwer auffindbar – Ranking-Potenzial bleibt ungenutzt. **Relevanz für uns:** Das ist derselbe Seitentyp (Bundesland-/Themen-Longtail), den wir bei beamtenservice als Content-Lücke notiert haben (Abschnitt „Top-Seiten" oben, „Bearbeitungsstand Beihilfe [Bundesland]"). Wenn wir vergleichbare Seiten bauen und sie konsequent intern verlinken, haben wir dort einen strukturellen Vorteil gegenüber beamtenberater.
2. **8 Noindex-Seiten in der Sitemap** (Error) – ausschließlich Rechtsseiten: `impressum`, `impressum-baufinanzierung`, `datenschutz`, `datenschutz-baufinanzierung`, `widerspruch`, `erstinformation`, `ki-transparenz`, `service/kontakt`. Technisch unsauber (Sitemap sollte nur indexierbare Seiten enthalten), aber ohne SEO-Relevanz.
3. **75 Seiten mit internen Links auf Redirects** (Warning), darunter Startseite, Blog, Rechner, `berufsgruppen/lehrer`. Bestätigt, dass die bereits unter „Befund vom 08.10.2026" vermutete URL-Migration (Wegfall des abschließenden Slashes) technisch noch nicht vollständig nachgezogen ist – interne Links zeigen weiterhin auf alte URLs statt direkt auf die neuen Ziel-URLs.
4. **71 Seiten, bei denen der von Google angezeigte Title vom Page-Title abweicht** (Notice) – Hinweis auf zu generische/schwache Title-Tags, die Google eigenständig umschreibt.
5. **179 Seiten mit unvollständigen Open-Graph-Tags** (Warning, größte Einzelgruppe) – betrifft nur die Social-Sharing-Darstellung, kein direkter Rankingfaktor.

**Einordnung:** Technisch insgesamt solide, aber nicht makellos (Health Score 81 vs. unsere 99). Die auffälligste strukturelle Schwäche ist die interne Verlinkung ihrer Longtail-Seiten (76 Orphans) – kombiniert mit dem Spam-Linkaufbau und dem Traffic-Rückgang (siehe oben) ein weiteres Indiz, dass beamtenberater aktuell eher mit Altlasten kämpft als systematisch zu wachsen.

## PDF-Report für Sven (08.10.2026)

Vollständige, grafisch aufbereitete Fassung dieser Analyse (Kennzahlen-Vergleich, Traffic-Verlauf, Backlink-/Spam-Analyse, Keyword- und Content-Gap, technischer Site-Audit, Website-Deep-Dive, Einordnung & Empfehlungen) als PDF erstellt: [[07 Anhänge/Wettbewerbsanalyse beamtenberater.com - 2026-10-08.pdf]].

## Gegencheck von Sven (08.10.2026, Traffic-Analyse via Jens Kempf)

Sven hat unsere Analyse mit einer eigenen Prüfung gegengelesen und bestätigt sowie präzisiert den Befund zum Traffic-Anstieg:

**Bestätigt:** Der Anstieg von ~1,9K auf 3,7K ist die Erholung ab dem Tiefpunkt im August, kein durchgehender Aufwärtstrend – seit Jahresanfang verliert die Seite eigentlich Traffic. Domain Rating blieb im selben Zeitraum stabil (27 → 30 → 29), also kein Linkaufbau-Effekt (deckt sich exakt mit unserem Befund oben).

**Neue Präzisierung – was den Anstieg tatsächlich auslöst:** Nicht Backlinks, sondern neue Inhalte. Die Zahl rankender Seiten sprang von 126 (Juli) auf 187 (August) – deckt sich mit unserer eigenen `pages-history`-Messung. Die `last_update` der neuen Keywords liegt durchgängig im September, die Seiten begannen also ab September/Oktober zu ranken. Stärkste neue Treiber, alle erst seit Ende August/September gelistet:

1. **„Bearbeitungsstand Beihilfe [Bundesland]"-Serie** – eigene Seite pro Bundesland (Berlin, Schleswig-Holstein, Hessen, NRW, Thüringen …). Berlin allein: ~336 Besucher/Monat, Position 4, Suchvolumen 2.200. Mit Abstand größter Einzelhebel.
2. „Kindergeld Beamte" – 827 Besucher, Position 2, Volumen 600.
3. „Dienstunfähigkeit Beamte" – 217 Besucher, Position 1, Volumen 1.000.
4. Weitere Grundlagenseiten: Beamter auf Lebenszeit/Widerruf, Heilfürsorge NRW, Krankenversicherung-Kosten für Beamte, Kindernachversicherung.

**Das Muster:** Eine programmatische Content-Serie zu Beamtenrecht- und Verwaltungsfragen – vor allem Status-/Bearbeitungsabfragen zu Beihilfe-Anträgen je Bundesland plus allgemeine Beamtenrecht-Grundlagenartikel. Keine dieser Seiten verkauft eine Versicherung direkt.

**Wichtige Verbindung zu unserer eigenen Strategie:** Das bestätigt unabhängig, was [[03 Bereiche/03 Bereiche (mein SEO Kram)/Content Creation/Content-Plan/Content-Roadmap 2027.md|Content-Roadmap 2027]] bereits aus den eigenen Zahlen ableitet: Beamtenrecht-Themen ziehen stärker als Versicherungsthemen – `/familienzuschlag-fuer-beamte/` schlägt bei uns den gesamten Beihilfe-Baukasten um das 3,6-Fache. Kempf bestätigt das Muster mit einem eigenen, noch spitzeren Cluster: Bearbeitungsstand-Abfragen sind ein Nachfragesignal mit echtem Volumen (80–2.200/Monat je Bundesland) und offenbar noch nicht gesättigt.

**Neue Erkenntnis zu AI Overviews:** Fast alle neuen Rankings von beamtenberater haben `ai_overview` als SERP-Feature – und ranken trotzdem organisch auf Position 1–2 mit echtem Traffic. Erklärung: Die Seiten beantworten eine sehr konkrete, oft verwaltungsbezogene Frage direkt und strukturiert (Frage-Antwort-Format, `question`-Feature fast überall vertreten). Das macht sie sowohl AI-Overview-tauglich als auch klick-tauglich für Nutzer, die über die Zusammenfassung hinaus die Originalquelle brauchen (z. B. um den tatsächlichen Bearbeitungsstand einer Behörde zu prüfen). Nicht trotz, sondern **mit** dem KI-Modus – relevant für die generelle AI-Overview-Sorge aus dem Status-Report.

**Offener Punkt von Sven, keine Entscheidung:** Soll die „Bearbeitungsstand Beihilfe [Bundesland]"-Lücke für fairbeamtet.de als eigenes Thema in der Content-Roadmap geprüft werden? Kein PKV-Beratungsinhalt, reine Verwaltungsinfo – ein Nachfragefeld, das aktuell kaum jemand außer Kempf bedient.

## Website-Deep-Dive vom 08.10.2026 (Nachtrag: Live-Prüfung der Seiten selbst, nicht nur Ahrefs-Zahlen)

Live-Abruf von Startseite, Team-Seite und Content-Beispielen beider Domains, abgeglichen mit Ahrefs-Rankingdaten einzelner URLs. Hinweis: kein Browser-Screenshot in dieser Session verfügbar, Design-Einschätzung beruht auf Seiteninhalt/-struktur, nicht auf visueller Begutachtung.

**Trust- und Markenauftritt (Startseite):** Auf dem Papier ist unser eigener Social-Proof-Auftritt mindestens gleichwertig, bei den harten Zahlen sogar deutlich stärker: 20.000+ Online-Beratungen / 4.700+ Kunden / 98 % Zufriedenheit / 1.007 Bewertungen (Trustindex, 4,9★) / sichtbare Makler-Registernummer (D-6TF6-JBEPB-55) bei uns vs. 5.000+ Beratene / 127 Google-Bewertungen (4,9★) / § 34d ohne sichtbare Registernummer bei beamtenberater. Einziger Pluspunkt bei denen: Der Provisions-/Interessenkonflikt-Hinweis steht bei beamtenberater prominent auf der Startseite, bei uns eher in der FAQ versteckt – leicht nachziehbar.

**Content-Tiefe im direkten Vergleich (Fallbeispiel „Kindergeld für Beamte"):** Gegenprobe mit Live-Ahrefs-Daten für die inhaltsgleichen Zielseiten:

| Merkmal | beamtenberater.com /kindergeld-beamte | fairbeamtet.de /kindergeld-fuer-beamte/ |
|---|---|---|
| Wortzahl (gesch.) | ~1.500 | ~4.500–5.500 |
| Tabellen | keine | 2 |
| FAQ-Fragen | 5 | 7 |
| Rankende Keywords (Ahrefs) | 30 | 11 |
| Traffic/Monat (Ahrefs, DE) | 851 | 124 |
| Backlinks auf die Seite | 8 (von 8 Domains) | **0** (live und all-time) |

**Wichtigster Einzelbefund:** Trotz rund dreifacher Wortzahl, zwei zusätzlicher Tabellen und mehr FAQ-Fragen bekommt unsere Seite 85 % weniger Traffic und rankt nur für gut ein Drittel der Keywords der kürzeren beamtenberater-Seite. Der Unterschied ist nicht der Inhalt, sondern die Backlinks: unsere Seite hat 0, die von beamtenberater 8. Das deckt sich mit dem bereits dokumentierten Befund bei `/beihilfe-berlin/` (ebenfalls 0 Backlinks trotz starkem Content, siehe [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]], Eintrag 06.10.2026) – zwei unabhängige Stichproben zeigen dasselbe Muster. Sieht nach einem strukturellen Problem aus (fehlende interne/externe Verlinkung nach Veröffentlichung), nicht nach einem Content-Qualitätsproblem.

**Content-Format-Lücke:** Die „Bearbeitungsstand Beihilfe [Bundesland]"-Seiten von beamtenberater bedienen eine eigenständige, transaktionsnahe Suchintention („Wo steht mein Antrag gerade?") statt der klassischen Ratgeber-Intention. Kein Qualitätsunterschied, sondern ein bei uns komplett fehlendes Content-Format – ließe sich grundsätzlich auch auf andere Verwaltungsvorgänge übertragen (z. B. Dienstunfähigkeits-Anträge, Umzugskostenerstattung).

**Design/UX (mit Einschränkung):** beamtenberater nutzt durchgängig "digital gestaltete" Symbolbilder, schlichte Farbpalette, klar visualisierten 4-Schritte-Beratungsprozess. fairbeamtet setzt auf das Cartoon-Maskottchen "Sven" (Varianten: Pilot, Wizard, Jedi) als durchgängige visuelle Identität – verspielter/zugänglicher. Bei einem YMYL-Versicherungsthema kann das je nach Zielgruppe sympathisch oder zu wenig seriös wirken; reine Stilfrage, aber einen Blick wert, ob das Maskottchen auf den nüchternen PKV-/BU-Seiten genauso gut funktioniert wie auf der Startseite.

**Fazit Deep Dive:** beamtenberater gewinnt **nicht** durch bessere Inhalte, mehr Social Proof oder cleverere CTAs – in allen drei Punkten stehen wir mindestens gleichauf, bei den Trust-Zahlen klar besser. Der reale Unterschied liegt in zwei strukturellen, gezielt angehbaren Punkten: (1) fehlende Backlinks/interne Verlinkung auf einzelne, auch inhaltlich starke Content-Seiten bei uns, und (2) ein bei uns komplett fehlendes Content-Format (kurze, transaktionsnahe Status-/Themenseiten).

## Nächste Schritte

- [ ] Monatlich gegenchecken, ob sich der Traffic-Rückgang stabilisiert oder weiter fällt (gleicher Turnus wie [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Los-Schmerz-Wochos.md|Los-Schmerz-Wochos]])
- [ ] Beobachten, ob die Spam-Linkwelle weitergeht oder ein Einzelereignis war
- [ ] Mit Sven klären: „Bearbeitungsstand Beihilfe [Bundesland]"-Lücke als eigenes Thema in [[03 Bereiche/03 Bereiche (mein SEO Kram)/Content Creation/Content-Plan/Content-Roadmap 2027.md|Content-Roadmap 2027]] aufnehmen? Sven hat das als offenen Punkt zurückgespielt (08.10.2026) – ist bei beamtenberater der mit Abstand größte Traffic-Treiber seit September und bestätigt unabhängig die „Beamtenrecht schlägt Versicherung"-These der Roadmap. Überschneidung mit der bereits notierten „Beihilfe pro Bundesland"-Lücke bei beamtenservice klären, evtl. zusammenlegen
- [ ] Bei eigenen Bundesland-/Themen-Longtail-Seiten von Anfang an auf saubere interne Verlinkung achten – beamtenberater hat laut Site-Audit-Crawl vom 08.10.2026 genau in diesem Seitentyp 76 verwaiste (nicht intern verlinkte) Seiten, das ist eine ausnutzbare Schwäche
- [ ] Bestehende starke Content-Seiten ohne Backlinks gezielt stärken statt neue, noch längere Artikel zu schreiben – mind. 2 Stichproben (`/kindergeld-fuer-beamte/`, `/beihilfe-berlin/`) zeigen 0 Backlinks trotz starkem Content (siehe Website-Deep-Dive oben). Interne Verlinkung mit passendem Anker + gezielter externer Linkaufbau priorisieren
- [ ] Entscheiden, ob dieses Projekt Ende Q4 2026 abgeschlossen oder weitergeführt wird
- [ ] Wichtiger als beamtenberater: eigenen Traffic-Rückgang (−52 % seit August 2026) untersuchen – ist das bei uns auch eine technische Ursache (Migration, Indexierung) oder reiner AI-Overview-Effekt? An [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Los-Schmerz-Wochos.md|Los-Schmerz-Wochos]] zurückspielen
- [ ] Verifizieren, ob AI Overviews tatsächlich flächendeckend neu in der Beamten-Nische sind (z. B. via Brand Radar/SEOgets), statt nur aus den SERP-Features der Ahrefs-Stichprobe zu schließen

## Notizen

Rohdaten per Ahrefs API (Site Explorer, Ländefilter DE wo zutreffend) live gezogen am 08.10.2026.
