---
tags: [projekt, fairbeamtet]
status: aktiv
erstellt: 2026-09-23
---

# Wettbewerbsanalyse

## Ziel

Die Konkurrenz von fairbeamtet.de in allen relevanten Bereichen analysieren und überholen.

## Status

In Bearbeitung

## Nächste Schritte

- [ ] Spam-Anteil neuer Backlink-Domains bei Wettbewerbern prüfen (offen laut Status Report)
- [ ] Zugang zu Ahrefs/SEOgets über Sven klären (siehe [[04 Ressourcen/Google Search Console/Google Search Console.md|Google Search Console]]) – Voraussetzung für laufendes Monitoring mit echten Daten

## Bekannte Wettbewerber

Stand 02.10.2026, per Ahrefs geprüft und in Tiers eingeteilt (Keyword-Überschneidung mit fairbeamtet.de, Traffic, Domain Rating). Tier-Einteilung bei Bedarf im Monats-Check neu bewerten.

**Tier 1 – echte Rankingkonkurrenz, aktiv tracken:**

| Domain | DR | Traffic/Monat | Gemeinsame Keywords mit uns |
|---|---|---|---|
| beamtenservice.de | 7 | 3.216 | 115 |
| schlemann.com | 45 | 20.889 | 24 |
| beamtenberater.com | 29 | 3.944 | 66 |

Ausführliche, laufende Analyse von beamtenberater.com (Backlink-Spam-Welle Sept. 2026, Traffic-Verlauf, Top-Seiten) jetzt in eigenem Projekt: [[02 Projekte/Fairbeamtet/Beamtenberater.com.md|Beamtenberater.com]].
| info-beihilfe.de | 29 | 7.172 | 48 |
| beamten-infoportal.de | 34 | 6.100 | 31 |

**Tier 2 – klein, gleiche Nische, im Blick behalten:**

- versicherungsvergleich-beamte.de (DR 36, 1.131 Traffic/Monat, 26 gemeinsame Keywords)
- optinvest-beamte.de (DR 27, 1.002 Traffic/Monat, 34 gemeinsame Keywords)
- beamtencircle.de (113 Keywords, 473 Traffic/Monat)
- onecept.de (DR 8, 629 Traffic/Monat, 21 gemeinsame Keywords)
- beamtenberatung-plus.de (110 Keywords, 645 Traffic/Monat)

**Tier 3 – beobachten, aber keine echte Rankingkonkurrenz (0 gemeinsame Keywords mit uns):**

- **alexander-kuhlen.de** ("Kuhlen", https://www.alexander-kuhlen.de/) – allgemeiner Versicherungsmakler, nur am Rande Beamten-Content. Kein akuter Traffic-Rivale, aber lehrreicher Negativ-Case: Traffic brach ab Okt. 2025 um −71 % ein (Höhepunkt 2.394 → aktuell 682 Besuche/Monat), vor allem Long-Tail-Rankings Platz 11+ (2.493 → 22 Keywords). Als Reaktion wurden ab Mai 2026 die Referring Domains von 112 auf 640 versechsfacht (+471 %) – zeitlich *nach* Beginn des Einbruchs, nicht davor. Der Traffic fiel trotzdem weiter. Klarer Beleg: Linkaufbau nach Menge als Reaktion auf einen Rankingverlust bringt nichts. Content-stilistisch bemerkenswert: durchgehende Du-Ansprache, starke Ich-Perspektive, persönliche Positionierung als unabhängiger Einzelmakler – funktioniert bei fairbeamtet als Team nicht 1:1, da wir mit mehreren namentlichen Beratern statt einer Einzelperson auftreten (siehe [[00 Kontext/Fairbeamtet/Team.md|Team]]).
- **derfairsicherungsladen.de** – DR 27, 35.049 Traffic/Monat, aber 0 gemeinsame Keywords. Allgemeiner Versicherungsmakler (Zahnzusatz, Wohngebäudeversicherung, Rentenlücke), keine Beamten-Nische.
- **versicherungenmitkopf.de** – DR 57, 35.049 Traffic/Monat, aber 0 gemeinsame Keywords. Fokus auf Rente/Pension allgemein (Rentenpunkte, Rente mit 63, Grundrente), nur am Rande Beamte. Als Content-Inspiration für Pensions-Themen trotzdem interessant.

Backlink- und Ranking-Vergleich (ursprünglich beamtenservice/beamtenberater/Kuhlen): siehe [[02 Projekte/Fairbeamtet/SEO-GEO Status Report.md|SEO-GEO Status Report]] (Abschnitt „Wettbewerbsanalyse: Linkwachstum vs. Ranking-Erfolg"). Kernbefund dort: Linkwachstum lief bei beamtenberater und Kuhlen gegenläufig zum Ranking-Erfolg – nur beamtenservice war zum damaligen Zeitpunkt stabil, hat dabei aber Links verloren. Die aktuelle Detailprüfung von Kuhlen (oben) bestätigt und verschärft das: sein Linkaufbau war sogar noch größer (+471 % statt der ursprünglich notierten +147 %) und eindeutig eine verspätete Reaktion auf den bereits laufenden Absturz, kein Auslöser für Erfolg.

## Monitoring (laufend)

Turnus: monatlich (Datum anpassen, sobald Tool-Zugang steht). Neue Befunde immer als zusätzliche Zeile in der Tabelle unten ergänzen, nicht bestehende Zeilen überschreiben – so bleibt der Verlauf sichtbar.

Was wir im Blick behalten:
- **Rankings**: Positionen zu unseren Kern-Keywords im Vergleich zu den drei Wettbewerbern
- **Backlinks**: Neue Domains, Spam-Anteil, Linkverluste (siehe offener Punkt oben)
- **Content**: Neue Artikel/Seiten der Wettbewerber, thematische Lücken bei uns
- **Positionierung/Messaging**: Änderungen an Angebot, Zielgruppenansprache

Quellen: Ahrefs, SEOgets (Search Console + GA4) – sobald Zugang von Sven da ist.

| Datum | Wettbewerber | Bereich | Befund | Aktion |
|---|---|---|---|---|
| 28.09.2026 | beamtenberater | Traffic/URL-Struktur | Ahrefs-Export (Top Pages, 282 Seiten) zeigt geschätzten Traffic von ~11.529 auf ~3.669 Besuche/Monat eingebrochen (−68 %). 162 Seiten als "Lost", 116 als "New" markiert – ein Teil davon ist vermutlich eine URL-Umstellung (Wegfall des abschließenden Slashes, z. B. `/kindergeld-beamte/` → `/kindergeld-beamte`), aber selbst die Paare zusammen zeigen echten Traffic-Rückgang, kein reines Zähl-Artefakt. Deckt sich mit dem Absturz-Befund aus [[02 Projekte/Fairbeamtet/SEO-GEO Status Report.md\|SEO-GEO Status Report]] (+153 % Backlinks, −60 % Top-3 bei beamtenberater). Rohdaten: [[07 Anhänge/beamtenberater.com-top-pages-subdomains-all_2026-09-28_09-47-06.csv]] | Beobachten, ob sich der Rückgang nach der URL-Umstellung stabilisiert oder weiter fällt |
| 02.10.2026 | beamtenservice | Keywords/Traffic/Content | Direkter Ahrefs-Vergleich: DR 7 vs. unsere 5,0; 796 vs. 370 organische Keywords; 3.216 vs. 1.498 Traffic/Monat; Keyword-Gap 681 (nur beamtenservice) vs. 254 (nur wir). Haupttreiber: systematische „Beihilfe [Bundesland]"-Seiten für praktisch jedes Bundesland (z. B. „beihilfe nrw" 9.300 Suchvolumen/Monat, Keyword-Schwierigkeit 0) – wir haben keine vergleichbaren Landes-Seiten. | Content-Lücke „Beihilfe pro Bundesland" als eigenes Vorhaben prüfen |
| 02.10.2026 | schlemann.com | Neu entdeckt | Bisher nicht auf der Konkurrenzliste. DR 45, 791 Keywords, 20.889 Traffic/Monat – größter Traffic-Wert aller geprüften Tier-1-Konkurrenten. 24 gemeinsame Keywords mit uns. | In Tier 1 aufgenommen, künftig mitverfolgen |
| 02.10.2026 | alexander-kuhlen.de (Kuhlen) | Backlinks/Traffic-Historie | Monatshistorie geprüft: Traffic-Einbruch begann bereits Okt. 2025 (−71 % bis heute, v. a. Long-Tail-Keywords Platz 11+ von 2.493 auf 22). Referring Domains explodierten erst ab Mai 2026 (112 → 640, +471 %) – zeitlich *nach* Einbruchsbeginn, also Reaktion statt Ursache. Traffic fiel trotz Linkaufbau weiter. Bestätigt und verschärft die bisherige Notiz (dort nur +147 % notiert). | Keine Aktion – dient als Negativ-Beispiel gegen Linkaufbau nach Menge |
| 06.10.2026 | beamtenservice (Benchmark) + eigene Seite | Backlinks/Content-Struktur | beamtenservice.de verliert aktuell massiv: organischer Traffic −52 % seit März 2026 (7.293 → 3.222/Monat), Top-3-Keywords fast halbiert (567 → 294), trotz Backlink-Aufbau (Referring Domains zeitweise auf 1.095). Gleichzeitig Detailprüfung unserer eigenen Seite `/beihilfe-berlin/`: Content ist stark (E-E-A-T, Tabellen, 2.500+ Wörter), rankt aber für „beihilfe berlin" (10.000 Vol./Monat) gar nicht (nicht in Top 11), nur für 3 Nebenvarianten. Ursache 1: 0 Backlinks auf die Seite, jemals – selbst der schwächste Konkurrent in der SERP (beamtenservice, DR 7) hat mind. 1. Ursache 2: Keyword-Kannibalisierung – Relevanz verteilt sich auf 3 eigene URLs (`/beihilfe-berlin/`, `/beihilfe-berlin-app/`, `/beihilfestelle-berlin/`), keine zielt direkt auf den Hauptbegriff; zudem fehlen FAQ-Blöcke zu den 4 „People also ask"-Fragen, die aktuell in der SERP erscheinen. | Backlinks/interne Verlinkung mit Anker „Beihilfe Berlin" auf die Hauptseite aufbauen; App- und Beihilfestelle-Seite in die Hauptseite integrieren oder stark verlinken; FAQ-Block mit den 4 PAA-Fragen ergänzen. Als Vorlage für die Analyse der anderen Bundesland-Seiten (NRW, Hessen, Thüringen) nutzen |
| 08.10.2026 | beamtenberater | Backlinks/Traffic | Live-Ahrefs-Check erklärt den scheinbaren Anstieg der verweisenden Domains (Aug. 487 → Okt. 968, +99 %): über 50 davon sind am 28./29.09.2026 neu registrierte `.shop`-Domains mit DR 0, von Ahrefs als `is_spam: true` markiert, je 1 Link, 0 eigener Traffic – eine Spam-Link-Welle, keine echte Kampagne. Domain Rating stieg trotzdem nicht (Peak 31 im Jan. 2026, jetzt 29). Echter organischer Traffic (DE) fällt weiter: von ~11.509/Monat (Aug. 2025) auf ~2.872/Monat (Okt. 2026), ca. −75 % seit Peak. Details: [[02 Projekte/Fairbeamtet/Beamtenberater.com.md|Beamtenberater.com]]. | Keine Aktion unsererseits nötig – dient als weiteres Negativ-Beispiel gegen Linkaufbau nach Menge; monatlich gegenchecken, ob sich der Traffic stabilisiert |
| 08.10.2026 | beamtenberater vs. alle Tier-1-Konkurrenten + wir | Traffic-Vergleich Aug.→Okt. 2026 | Im kurzfristigen Vergleich ist beamtenberater die einzige Domain mit Traffic-Anstieg (+74 %, 1.649→2.872), während beamtenservice (−49 %), info-beihilfe (−46 %), beamten-infoportal (−48 %) und **fairbeamtet selbst (−52 %, 2.338→1.117)** im selben Fenster fielen; schlemann blieb flach. Ursache ist kein Wettbewerbsvorteil: Top-Pages-Vergleich zeigt, dass beamtenberater zeitgleich eine URL-Migration durchlief (Wegfall des abschließenden Slashes, z. B. `/kindergeld-beamte/` → `/kindergeld-beamte`) – der Anstieg ist die Erholung vom eigenen Migrations-Einbruch, kein Wachstum über das Vor-Krise-Niveau (März 2026: 4.180) oder das Allzeithoch (Aug. 2025: 11.509) hinaus. Fast alle geprüften Keywords zeigen inzwischen das SERP-Feature `ai_overview` – mögliche Mit-Ursache für den branchenweiten Rückgang bei allen anderen. Details: [[02 Projekte/Fairbeamtet/Beamtenberater.com.md|Beamtenberater.com]]. | Wichtiger als beamtenberater: eigenen Rückgang (−52 % seit Aug. 2026) priorisiert untersuchen – an [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Los-Schmerz-Wochos.md\|Los-Schmerz-Wochos]] zurückspielen |
| 08.10.2026 | beamtenberater | Content-Treiber (Gegencheck Sven/Jens Kempf) | Sven hat den Traffic-Anstieg gegengeprüft: Auslöser sind neue Inhalte, nicht Backlinks (DR stabil 27→30→29). Rankende Seiten sprangen von 126 (Juli) auf 187 (August), `last_update` der neuen Keywords liegt durchgängig im September. Größter Einzelhebel: eine „Bearbeitungsstand Beihilfe [Bundesland]"-Serie je Bundesland (Berlin allein ~336 Besucher/Monat, Pos. 4, Vol. 2.200), dazu „Kindergeld Beamte" (827 Besucher, Pos. 2) und „Dienstunfähigkeit Beamte" (217 Besucher, Pos. 1). Bestätigt unabhängig die These aus [[03 Bereiche/03 Bereiche (mein SEO Kram)/Content Creation/Content-Plan/Content-Roadmap 2027.md\|Content-Roadmap 2027]]: Beamtenrecht-Themen ziehen stärker als Versicherungsthemen. Zusatzbefund: Die neuen Seiten ranken trotz `ai_overview`-SERP-Feature organisch auf Pos. 1–2, weil das Frage-Antwort-Format sowohl AI-Overview-tauglich als auch klick-tauglich ist. Details: [[02 Projekte/Fairbeamtet/Beamtenberater.com.md\|Beamtenberater.com]]. | Entschieden: „Bearbeitungsstand Beihilfe [Bundesland]"-Lücke als eigenes Thema in [[03 Bereiche/03 Bereiche (mein SEO Kram)/Content Creation/Content-Plan/Content-Roadmap 2027.md\|Content-Roadmap 2027]] aufgenommen |

## Notizen

