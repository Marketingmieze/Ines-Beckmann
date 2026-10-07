---
tags: [projekt, fairbeamtet, los-schmerz-wochos]
status: aktiv
erstellt: 2026-10-07
---

# Fortschritt-Notizen Content-Plan

Ausführliche Ergebnisse, Befunde und Zusatzinfos zu den Aufgaben aus [[Content-Plan]]. Der Content-Plan selbst bleibt strukturell nah am Original-PDF von Sven ([[07 Anhänge/Content-Plan fairbeamtet.de 2026-09-30.pdf]]) und zeigt nur noch Haken + kurze Verweise auf diese Datei.

---

## Claude-Hinweis (Woche 1 – Brand Radar mit Prompts füllen)

Hinweis 07.10.2026: Claude verbraucht pro Prompt und Update 8 Prüfungen, jede andere Plattform (ChatGPT, Übersicht mit KI, KI-Modus, Gemini, Perplexity, Copilot) nur 1. Grundplan hat 300 Prüfungen/Monat. Bei 25 Prompts × 6 Plattformen × wöchentlich sind es bereits 600/Monat – also schon ohne Claude über dem Kontingent. Mit Claude dazu (25 × 4 × 14) sind es 1.400/Monat. Mehrkosten über Pay-as-you-go (€0,0187/Prüfung): ohne Claude ca. €5,61/Monat, mit Claude ca. €20,57/Monat – vorausgesetzt Pay-as-you-go ist aktiviert, sonst wird das Tracking bei Kontingent-Ende vermutlich gekappt. Vor dem Umschalten prüfen: Pay-as-you-go an, oder Frequenz/Prompt-Anzahl reduzieren.

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
