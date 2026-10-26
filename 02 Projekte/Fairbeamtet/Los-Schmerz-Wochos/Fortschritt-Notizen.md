---
tags: [projekt, fairbeamtet, los-schmerz-wochos]
status: aktiv
erstellt: 2026-10-07
---

# Fortschritt-Notizen Content-Plan

Ausführliche Ergebnisse, Befunde und Zusatzinfos zu den Aufgaben aus [[Content-Plan]]. Der Content-Plan selbst bleibt strukturell nah am Original-PDF von Sven ([[07 Anhänge/Content-Plan fairbeamtet.de 2026-09-30.pdf]]) und zeigt nur noch Haken + kurze Verweise auf diese Datei.

---

## Eigener Traffic-Rückgang (−52 % seit August) — Untersuchung 12.10.2026

Auftrag aus dem 08.10.-Befund bei [[02 Projekte/Fairbeamtet/Beamtenberater.com|Beamtenberater.com]]: der eigene Rückgang wurde als wichtiger eingestuft als alles beim Wettbewerber und sollte hierher zurückgespielt werden.

**Daten (SEO Gets, GSC+GA4, 14-Tage-Durchschnitt 01.–14.07.2026 vs. 27.09.–10.10.2026):**

| Metrik | Juli | Okt | Veränderung |
|---|---|---|---|
| Klicks/Tag | 235,0 | 129,4 | −45 % |
| Impressionen/Tag | 12.058 | 7.511 | −38 % |
| CTR | 1,95 % | 1,72 % | −12 % |
| Position | 9,95 | 8,53 | **besser** |

**Befund: Kein Ranking-Problem.** Die durchschnittliche Position hat sich im selben Zeitraum verbessert, nicht verschlechtert. Der Rückgang ist ein Klick-/Impressions-Problem, kein Sichtbarkeits-Problem im klassischen Sinn.

**Auf Seitenebene konzentriert sich der Rückgang auf wenige große informationelle Seiten**, die zusammen ca. 60 % des gesamten Klickrückgangs ausmachen:

| Seite | Klicks Juli → Okt | Position Juli → Okt |
|---|---|---|
| /familienzuschlag-fuer-beamte/ | 1.345 → 924 (−31 %) | 4,19 → 3,35 (besser) |
| /kindergeld-fuer-beamte/ | 356 → 127 (−64 %) | 3,96 → 2,92 (besser) |
| /amtsaerztliche-untersuchung/ | 343 → 103 (−70 %) | 6,80 → 6,65 (besser) |
| /beitragsrueckerstattung-debeka/ | 260 → 115 (−56 %) | 5,20 → 4,97 (besser) |
| Startseite / | 138 → 81 (−41 %), Impressionen −76 % | 29,77 → 30,96 (leicht schlechter) |

Bei allen vier großen Nicht-Startseiten ist die Position stabil oder besser geworden, während die Klicks zweistellig bis −70 % einbrachen. Das ist dieselbe Signatur wie der Zero-Click/KI-Übersicht-Befund vom 07.10. bei der Debeka-Testseite (dort: bei allen 5 geprüften Anfragen großer KI-Kasten, fairbeamtet fast nie zitiert) — Familienzuschlag, Kindergeld und Amtsärztliche Untersuchung sind klassische kurze Fakten-Fragen, die Google bevorzugt direkt in der KI-Übersicht beantwortet.

**Eingeordnet, nicht abschließend bewiesen:** Die GSC/GA4-Daten zeigen nur die Korrelation (Position stabil/besser, Klicks eingebrochen), nicht direkt die Ursache. Zusätzlich lagen im Zeitraum zwei Google-Updates: August 2026 Spam Update (Rollout abgeschlossen 21.08.) und September 2026 Spam Update (Rollout 24.09.–08.10.) — zeitlich correlieren beide mit Phasen des Rückgangs, ohne dass sich daraus allein eine Kausalität ableiten lässt.

**Nächster Schritt:** Wie bei der Debeka-Testseite (Schritt 0) direkt in der Google-Suche prüfen, ob bei "familienzuschlag beamte", "kindergeld beamte" und "amtsärztliche untersuchung beamte" ein KI-Übersichtskasten erscheint und ob/wie oft fairbeamtet.de darin zitiert wird.

---

## Claude-Hinweis (Woche 1 – Brand Radar mit Prompts füllen)

Hinweis 07.10.2026: Claude verbraucht pro Prompt und Update 8 Prüfungen, jede andere Plattform (ChatGPT, Übersicht mit KI, KI-Modus, Gemini, Perplexity, Copilot) nur 1. Grundplan hat 300 Prüfungen/Monat. Bei 25 Prompts × 6 Plattformen × wöchentlich sind es bereits 600/Monat – also schon ohne Claude über dem Kontingent. Mit Claude dazu (25 × 4 × 14) sind es 1.400/Monat. Mehrkosten über Pay-as-you-go (€0,0187/Prüfung): ohne Claude ca. €5,61/Monat, mit Claude ca. €20,57/Monat – vorausgesetzt Pay-as-you-go ist aktiviert, sonst wird das Tracking bei Kontingent-Ende vermutlich gekappt. Vor dem Umschalten prüfen: Pay-as-you-go an, oder Frequenz/Prompt-Anzahl reduzieren.

Update 07.10.2026: Beim Review von [[Brand Radar Prompts]] wurden inhaltliche Lücken ergänzt (Berufsunfähigkeit-Themen, Beitragserhöhung, drei weitere Vorerkrankungen) – die Liste ist dadurch von 27 auf 35 Prompts gewachsen, auf Wunsch von Ines bewusst ohne das Budget-Problem jetzt zu lösen. Das verschärft die Kontingent-Rechnung oben weiter (35 × 6 × wöchentlich ≈ 840 Prüfungen/Monat ohne Claude, schon fast das Dreifache des 300er-Kontingents). Die Entscheidung über Frequenz (wöchentlich vs. monatlich), Prompt-Anzahl und Pay-as-you-go steht weiterhin offen und sollte vor dem Eintragen in Ahrefs getroffen werden.

**Realer Verbrauch 07.10.2026 (Widerspruch zur Schätzung oben):** Ines hat die ersten 12 Prompts (PKV allgemein + Testsieger + ein Teil Beihilfe) ins Ahrefs-UI eingetragen. Danach waren bereits 288 von 300 Prüfungen/Monat verbraucht – das sind rund 24 Prüfungen pro Prompt, deutlich mehr als die ursprüngliche Schätzung von 6/Prompt/Woche (vermutlich zusätzlicher Verbrauch durch einmaligen Backfill/Ersteinrichtung je Prompt, nicht nur laufendes wöchentliches Monitoring). Nur noch 12 Prüfungen übrig. Die restlichen 23 Prompts der Liste sind **nicht mehr eingetragen** und können beim aktuellen Verbrauchstempo nicht mehr ins Grundkontingent passen (23 × 24 ≈ 552 weitere Prüfungen nötig). Wichtig: Diese 288 Prüfungen sind komplett ohne Claude als Datenquelle entstanden (Schalter steht noch auf "off") – Claude würde den Verbrauch zusätzlich verschärfen, da es laut Claude-Hinweis oben 8 Prüfungen pro Prompt/Update kostet statt 1 wie bei den anderen sechs Plattformen. Rückmeldung an Sven vorbereitet, Entscheidung (Monatsreset abwarten vs. Pay-as-you-go) steht noch aus.

**Status 12.10.2026:** Nachricht an Sven verschickt. Rückmeldung von ihm steht weiterhin aus.

---

## Marken-Kannibalisierung (Woche 1)

**Prüfen, welche Seiten für 'fairbeamtet' ausgespielt werden — ✅ 2026-10-07**

Ergebnis 07.10.2026 (Search Console, letzte 3 Monate, Suchanfrage 'fairbeamtet', 61 Seiten gesamt): Startseite (HTTPS) 337 Klicks/674 Impressionen. Danach Team-Seite `/geschaeftsfuehrung-und-mitarbeiter/` 19/614, die unverschlüsselte `http://www.fairbeamtet.de/` 19/518, `/service/` 8/269, `/service/online-beratung/` 4/642, der Tipps-Artikel `/5-tipps-pkv-vergleich/` 4/597. Zusätzlich drei Experten-Profilseiten (Elenor Habtezghi, Dennis Kaspers, Sebastian Gottschalk) mit zusammen über 500 Impressionen bei nur 2 Klicks. Bestätigt die Vermutung aus dem Plan eins zu eins: Team-Seite, Online-Beratung und Tipps-Artikel nehmen der Startseite tatsächlich Sichtbarkeit weg. Auffällig zusätzlich: Online-Beratung hat mit 642 Impressionen sogar mehr als die Team-Seite.

**http://www.fairbeamtet.de/ auf HTTPS weiterleiten**

Beleg aus der Prüfung oben: `http://www.fairbeamtet.de/` sammelt allein 19 Klicks und 518 Impressionen für den Markennamen – fast so viel wie die Team-Seite.

---

## Vier Tippfehler-URLs aufräumen (Woche 1) — ✅ 2026-10-05

Erledigt: `/familienzuschlag-fuer-bebten/` und `/familienzuschlag-fuer-beamten/` → 301 auf `/familienzuschlag-fuer-beamte/`; `/debeka-or-dbv-pkv-beamte-vergleich/` → 301 auf `/debeka-oder-dbv-pkv-beamte-vergleich/`; `/fairbeamtet.de/familienzuschlag-fuer-beamte/` leitete schon vorher korrekt weiter. Per HTTP-Check am 05.10.2026 verifiziert.

---

## VideoObject auf /youtube/ ergänzen (Woche 1) — ⚠️ Prüfung 2026-10-05

Vermutlich falsche URL im Plan. Live-Check: `/youtube/` ist nur eine dünne Übersichtsseite ohne eigene Video-Einbettungen (kein Video markierbar, daher zu Recht kein Markup). Die eigentliche Video-Seite liegt eine Ebene tiefer unter `/youtube/youtube-pkv-videos-beamte/` und hat dort bereits vollständiges VideoObject-Markup für 20 Videos (mehr als die 7 aus der Sitemap), zuletzt bearbeitet 21.05.2026. Die 7 Sitemap-Videos selbst sitzen einzeln in Artikeln (z. B. `/pkv-beitragsanpassung-2025/`), dort generiert Rank Math das Markup automatisch. Aktuell kein Handlungsbedarf erkennbar – mit Sven abgleichen, ob er eine andere URL meinte.

---

## Zwei H1 auf der Vergleichsseite (Woche 1) — ✅ 2026-10-05

Konkretisiert 05.10.2026: Gemeinte Seite ist `/pkv-ratgeber/pkv-vergleich-beamte/` (per Live-Check gefunden: „Private Krankenversicherung für Beamte: Vergleich der wichtigsten Anbieter" und „PKV für Beamte: Vergleich der wichtigsten Anbieter" – auch die dünne „Linkliste" mit ~387 Wörtern Content aus Woche 2 ist dieselbe Seite). Laut Ines sind die zwei H1 responsive Varianten: eine nur für Desktop/Tablet, eine nur für Mobile sichtbar (per CSS ausgeblendet). Für Google ändert das nichts – beide stehen im HTML, CSS-Sichtbarkeit wird beim Crawling nicht berücksichtigt. Fix entsprechend nicht "Duplikat löschen", sondern eine der beiden `<h1>` auf `<h2>` (oder reines Styling-Element ohne Heading-Tag) herabstufen, responsive Verhalten bleibt erhalten.

## Datum auf der Vergleichsseite setzen (Woche 1)

Ergänzung 05.10.2026: Die Seite hat auch **keinen Autor** gesetzt – gehört eigentlich zur Woche-10-Aufgabe „Kontaktdaten und Autorenprofile prüfen", aber da man ohnehin hier ist, macht es Sinn, es mitzunehmen. Die Seite läuft über ein Elementor-Theme-Builder-Template; möglich, dass (1) der native WP-Autor am Beitrag nicht gesetzt ist oder (2) das Template gar kein Autor-Widget anzeigt. Eine Template-Änderung betrifft wahrscheinlich mehrere Ratgeber-Seiten gleichzeitig – deshalb bewusst Sven überlassen statt eigenständig am gemeinsamen Template zu ändern.

---

## Beihilfeergänzungstarif (Woche 7) — Korrektur 26.10.2026

Der Plan notiert für `beamtenservice.de/beihilfeergaenzungstarif-so-findest-du-den-besten-anbieter/` **1.813 Wörter**. **Das war zu niedrig geschätzt, aber in die falsche Richtung.** NeuronWriter zählt den Artikel beim Import in Svens Query (`784432dc018302b6`) exakt mit **1.146 Wörtern** – der Konkurrenzartikel ist also dünner als angenommen, nicht dicker. Zur Einordnung: eine eigene Web-Schätzung kam vorher auf 2.500–3.000 Wörter, ebenfalls daneben. NeuronWriters Zählung gilt als verlässlichste Quelle, weil sie den tatsächlichen Fließtext strukturiert erfasst statt grob zu schätzen.

Content-Erstellung für dieses Thema läuft bereits: [[03 Bereiche/03 Bereiche (mein SEO Kram)/Content Creation/Content Creatorin Claudia/artikel/2026-10-26_beihilfeergaenzungstarif/00_dossier.md|Artikel-Dossier]].
