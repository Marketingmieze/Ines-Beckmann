---
tags: [projekt, fairbeamtet, los-schmerz-wochos]
status: aktiv
erstellt: 2026-09-30
quelle: "07 Anhänge/Content-Plan fairbeamtet.de 2026-09-30.pdf"
autor: Sven Höhne
---

# Content-Plan fairbeamtet.de – 13-Wochen-Umsetzungsplan

Von Sven ausgearbeitet, Stand 30.09.2026, als PDF geliefert: [[07 Anhänge/Content-Plan fairbeamtet.de 2026-09-30.pdf]]. Grundlage laut PDF: Content-Roadmap 2027 und der Aufgabenblock „Website und Content Optimierungen". Die Reihenfolge folgt den zwei Etappen aus [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Los-Schmerz-Wochos.md|Los-Schmerz-Wochos]]: erst Beamtenservice.de überholen, dann Googles Nummer 1 werden.

## Aufwand und Ziel-Rechnung

- **Gesamtaufwand:** 509 Stunden über 13 Wochen
- Bei 40 h/Woche: ca. 3 Monate
- Bei 10 h/Woche nebenher: ca. 51 Wochen (knapp 12 Monate)
- Bis 31.12.2027 sind es 15 Monate – bei 10 h/Woche bleiben ca. 3 Monate Puffer. Knapp, aber machbar. Fällt die Arbeit drei Monate aus, ist der Puffer weg.
- Jede Zeitangabe enthält Recherche, Bilder/Tabellen, WordPress-Einpflegen und Korrekturlesen – nicht nur das Schreiben. Schätzungen sind eher großzügig; wo sie danebenliegen, eher zu niedrig.

## Woche 1 – Messen können und die schnellen Fixes (39,75 h)

- [ ] **Brand Radar mit Prompts füllen** (4,25 h) – läuft seit Mai leer, zeigt deshalb überall null
  - [ ] 20–30 Prompts formulieren (4 h) – echte Beamten-Fragen, nicht Keywords („Lohnt sich die PKV für mich als Lehrer?")
  - [ ] Claude als Datenquelle einschalten (0,25 h) – steht aktuell auf „off"
- [ ] **Beratungsanfrage in GA4 als Key Event einrichten** (4 h) – September: 3.146 Besucher, 0 gemessene Anfragen
  - [ ] Ziel definieren: welches Formular zählt (1 h) – Online-Beratung, Rückruf, oder beides
  - [ ] Event konfigurieren und als Key Event markieren (2 h)
  - [ ] Testen: Anfrage absenden, in GA4 nachsehen (1 h)
- [ ] **Rank Tracker erweitern** (3 h) – aktuell nur 20 Keywords, Ziel ist „überall Platz 1"
  - [ ] Kernbegriffe zusammenstellen (1,5 h) – 50–100 Kaufabsicht-Begriffe je Berufsgruppe
  - [ ] Keywords eintragen, beamtenservice.de als Wettbewerber anlegen (1,5 h)
- [ ] **Mitbewerberliste im Ahrefs-Projekt neu setzen** (1 h) – zwei der fünf hinterlegten Gegner tauchen bei Kernbegriffen gar nicht auf
  - [ ] Drei echte Wettbewerber aufnehmen (0,5 h) – versicherungsvergleich-beamte.de, beamtenpiloten.de, optinvest-beamte.de
  - [ ] beamtenberater.com und beamtencircle.de überprüfen (0,5 h) – raus oder begründen
- [ ] **Marken-Kannibalisierung auflösen** (7,5 h) – Startseite steht für „fairbeamtet" nur auf Platz 4,91 (vor einem Jahr: Platz 1)
  - [ ] Prüfen, welche Seiten für „fairbeamtet" ausgespielt werden (3 h) – Search Console, nach Seiten gruppieren
  - [ ] http://www.fairbeamtet.de/ auf HTTPS weiterleiten (1,5 h)
  - [ ] Startseite als eindeutige Markenseite kenntlich machen (3 h) – Titel, Beschreibung, Organisation-Markup
- [ ] **Sitemap ergänzen: `/pkv-ratgeber/`-Zweig fehlt** (1,5 h) – sechs rankende Seiten fehlen in der Sitemap, darunter die beste PKV-Seite
- [ ] **Weiterleitung `/bu-du/` korrigieren** (1 h) – Kategorie leitet fälschlich auf einen einzelnen Artikel statt Übersicht
- [ ] **Vier Tippfehler-URLs aufräumen** (1 h) – z. B. „familienzuschlag-fuer-bebten", auf 404 oder richtige Seite leiten
- [ ] **AggregateRating und FAQPage entfernen** (2 h) – Google zeigt beides nicht mehr (Sterne für eigene Firma ausgeschlossen, FAQ seit Mai abgeschafft)
- [ ] **Autoren-Slugs „bond-007" und „fairbeamtet" korrigieren** (2 h) – richtige Namen oder noindex
- [ ] **Zugang für KI-Crawler und Snippet-Freigabe prüfen** (1 h) – robots.txt/Meta-Tags, sonst kein Erscheinen in KI-Antworten
- [ ] **VideoObject auf `/youtube/` ergänzen** (2 h) – sieben Videos in der Video-Sitemap, aber kein Video-Markup auf der Seite
- [ ] **Zwei H1 auf der Vergleichsseite auf eine reduzieren** (0,5 h)
- [ ] **Datum auf der Vergleichsseite setzen** (0,5 h) – bislang weder Veröffentlichungs- noch Änderungsdatum
- [ ] **Vergütung auf der Vergleichsseite offenlegen** (0,5 h) – aktuell steht nur „kostenlos", nicht dass die Gesellschaft zahlt
- [ ] **Gruppe „PKV Test Gesellschaften" nach Position aufschlüsseln** (2 h) – 20.000 Impressionen, fast keine Klicks; erst prüfen, welche auf Platz 3–10 stehen, bevor Titel umgeschrieben werden
- [ ] **Kanal OPTINVEST Beamte auswerten** (4 h) – Wettbewerber besetzt mit vier YouTube-Videos den KI-Block beim wichtigsten Begriff
- [ ] **Erste Messzeile in [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Fortschritt.base|Fortschritt.base]] anlegen** (2 h) — **bereits erledigt:** siehe [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Messungen/2026-09.md|Messung 2026-09]]

## Woche 2 – Die Vergleichsseite, der direkte Zweikampf (37 h)

- [ ] **Material aus vier vorhandenen Seiten sichten** (4 h)
  - [ ] Testkritik aus den zwei Warentest-Artikeln ziehen (1,5 h) – stiftung-warentest-pkv-test-beamte-2025, finanztest-2019-pkv
  - [ ] Musterkunden-Argument herüberziehen (1,5 h) – von `/private-krankenversicherung/beamte/`
  - [ ] Annahmepolitik aus dem Debeka-Artikel holen (1 h) – debeka-beitragserhoehung-2025
- [ ] **Struktur festlegen** (2 h) – Gliederung vor dem Schreiben
- [ ] **Die Seite schreiben** (16 h) – aus 387 Wörtern Linkliste wird eine Seite, die selbst antwortet (Konkurrent: 4.315 Wörter, Platz 3)
  - [ ] Hauptantwort nach oben, dann „Das Wichtigste in Kürze" (3 h)
  - [ ] Testkritik als eigener Abschnitt (4 h)
  - [ ] Vergleichsrechner und Musterkunden (3 h)
  - [ ] Annahmepolitik und Beitragsstabilität (3 h)
  - [ ] Fazit mit Empfehlung und Offenlegung (3 h) – inkl. Courtage-Hinweis
- [ ] **Aktuellen Anlass setzen und datieren** (3 h) – Test, Ranking oder Beitragsanpassung als Aufhänger
- [ ] **Quellen verlinken** (2 h) – Stiftung Warentest, Check24, Verivox werden genannt, aber nicht verlinkt
- [ ] **Tabellen und Bilder bauen** (4 h)
- [ ] **Einpflegen, Korrektur lesen, Schema prüfen** (4 h)
- [ ] **Prüfen, welche der fünf verlinkten Seiten noch eine eigene Frage hat** (2 h)

## Woche 3 – Snippets und Redaktionsleitlinie (40 h)

- [ ] **Titel und Beschreibungen auf Position 3–10 überarbeiten** (15 h) – gesehen, aber nicht geklickt
  - [ ] Je Seite prüfen: Steht die Suchanfrage wörtlich im Titel? (6 h)
  - [ ] Beschreibungen aus dem Inhalt statt aus der Schablone (6 h) – konkrete Zahl statt Adjektive
  - [ ] Markenkonvention durchziehen (3 h) – einheitlich „Thema | fairbeamtet.de", Pfeilzeichen raus
- [ ] **Gruppe „BU Tipps & Tricks für Beamte" prüfen** (10 h) – 12 Seiten, 9.552 Impressionen, Ø-Position 31
- [ ] **Markenkonvention über alle übrigen Titel ziehen** (8 h)
- [ ] **Redaktionsleitlinie mit Courtage-Offenlegung schreiben** (7 h) – Seite `/redaktion/` existiert noch nicht
  - [ ] Entwurf: wie ihr arbeitet, wie ihr vergütet werdet (4 h)
  - [ ] Rechtlich gegenlesen lassen (1 h)
  - [ ] Seite anlegen und aus dem Fußbereich verlinken (2 h)

## Woche 4 – Was am 23. Juni verloren ging (40 h)

- [ ] **Die drei PKV-Seiten gegen die Wayback-Fassung vergleichen** (9 h) – wichtigste Seite fiel nach Neuerstellung am 23.6. von Position 12 auf 40
  - [ ] `/private-krankenversicherung/beamte/` (3 h)
  - [ ] `/private-krankenversicherung/beamtenanwaerter/` (3 h)
  - [ ] `/private-krankenversicherung/referendariat/` (3 h)
- [ ] **Entscheiden: wiederherstellen oder gezielt ergänzen** (2 h)
- [ ] **Die Entscheidung umsetzen** (20 h)
  - [ ] Seite PKV für Beamte (8 h) – 7.266 Impressionen, ein Klick
  - [ ] Seite PKV für Beamtenanwärter (6 h) – Position 41
  - [ ] Seite PKV im Referendariat (6 h) – Position 33
- [ ] **Zielseite für „Dienstunfähigkeitsversicherung für Beamte" festlegen** (4 h) – aktuell rankt dafür die Polizei-Seite
- [ ] **Cluster Vergleich, Test und Erfahrungen: Inventur** (5 h) – je Seite in einem Satz die beantwortete Frage notieren

## Woche 5 – Die Kostenseite und der Vergleichs-Cluster (40 h)

- [ ] **Seite „PKV Kosten für Beamte" neu bauen** (20 h) – alte Kostenseite brachte 1.174 Klicks/9 Monate, wurde dann umgeleitet
  - [ ] Alte Fassung aus der Wayback Machine sichten (2 h)
  - [ ] Struktur: Kostenfrage zuerst, dann Einflussfaktoren (2 h)
  - [ ] Schreiben mit Rechenbeispielen und Beitragsspannen (10 h)
  - [ ] Tabellen, Bilder, Einpflegen, Korrektur (6 h)
- [ ] **Alte URL auf die neue Kostenseite leiten** (1 h)
- [ ] **Cluster Vergleich, Test und Erfahrungen ordnen** (7 h) – bis zu 18 eigene Seiten konkurrieren um dieselbe Anfrage
  - [ ] Je Seite festlegen, welche Frage sie beantwortet (3 h)
  - [ ] Zusammenlegen oder abgrenzen, Weiterleitungen setzen (4 h)
- [ ] **Kostenfragen je Zielgruppe bedienen** (12 h) – stärkster Kaufabsicht-Begriff „private krankenversicherung kinder beamte kosten" (24 Klicks); Kostenseiten für Anwärter, Lehrer, Familien bauen

## Woche 6 – Transaktionsseiten: der fehlende Bottom-Funnel (40 h)

- [ ] **Risikovoranfrage starten** (12 h) – zweitwichtigster Schmerzpunkt, bislang keine Seite dafür
  - [ ] Prozess festlegen: was passiert nach dem Absenden (2 h)
  - [ ] Formular bauen, Datenschutzhinweise prüfen (5 h) – Gesundheitsdaten
  - [ ] Seitentext schreiben (4 h)
  - [ ] Testlauf mit einer echten Anfrage (1 h)
- [ ] **Beitragserhöhung prüfen lassen** (10 h) – Seite zum Hochladen/Prüfen des Erhöhungsschreibens
- [ ] **Tarifwechsel-Check** (10 h) – Tarifwechsel nach § 204, kaum bekannt
- [ ] **Unterlagen fürs Referendariat einreichen** (8 h) – Upload-Seite statt E-Mail

## Woche 7 – Die ersten zwei Themenlücken (38 h)

- [ ] **Beihilfeergänzungstarif** (20 h) – stärkste Konkurrenzseite (505 Besucher/Monat bei nur 1.813 Wörtern), wir haben dazu nichts; Suchvolumen zusammen über 1.100
  - [ ] Fachrecherche: wie der Tarif je Bundesland funktioniert (6 h)
  - [ ] Schreiben (9 h)
  - [ ] Tabellen je Bundesland, Einpflegen, Korrektur (5 h)
- [ ] **Öffnungsaktion und Öffnungsklausel PKV** (18 h) – 850 Suchen/Monat, wir Position 26–48, Konkurrent Platz 2
  - [ ] Fachrecherche: Bedingungen, Fristen, Nachteile (5 h)
  - [ ] Schreiben (8 h)
  - [ ] Einpflegen, Korrektur (5 h)

## Woche 8 – Dritte Themenlücke und die DU-Seiten (40 h)

- [ ] **Ruhegehalt bei Dienstunfähigkeit** (18 h) – 700 Suchen/Monat, aktuell null Impressionen
  - [ ] Fachrecherche: Berechnung, Versorgungsabschlag, Tabelle (6 h)
  - [ ] Schreiben mit Rechenbeispielen (8 h)
  - [ ] Tabelle bauen, Einpflegen, Korrektur (4 h)
- [ ] **DU Lehrer ordnen und ausbauen** (12 h) – Konkurrent Platz 1 bei „Dienstunfähigkeit Lehrer", unsere Seite heißt fälschlich „Berufsunfähigkeit Lehrer" (Position 28)
- [ ] **Zielseite „Dienstunfähigkeitsversicherung für Beamte" bauen** (10 h) – existiert nicht, deshalb rankt die Polizei-Seite

## Woche 9 – Vorlauf für eigene Daten und der Beihilfe-Hebel (40 h)

- [ ] **Datenschutz für die eigenen Auswertungen klären** (6 h) – Ablehnungsquoten/Zuschläge sind Gesundheitsdaten nach Art. 9 DSGVO
  - [ ] Welcher Aggregationsgrad ist zulässig? (3 h) – Datenschutzbeauftragten/Anwalt fragen, nicht raten
  - [ ] Datenschutzerklärung anpassen, falls nötig (3 h)
- [ ] **Prüfen, ob sich Quoten aus PW (Professional Works) auswerten lassen** (6 h) – wenn nicht, ist der ganze Hebel tot; das jetzt klären, nicht erst Woche 11
- [ ] **Die fünf Beihilfe-Seiten knapp vor Seite 1 nach vorn bringen** (20 h) – Position 13–24, zusammen 3.100 Suchen/Monat
  - [ ] beihilfestelle-berlin (4 h) – „landesverwaltungsamt berlin beihilfe", Position 24, 800 Suchen
  - [ ] beihilfe-berlin (4 h) – „beihilfe berlin pensionäre", Position 13, 600 Suchen (kürzester Weg auf Seite 1)
  - [ ] beihilfestelle-hessen (6 h) – zwei Begriffe, zusammen 1.100 Suchen, Position 18/20
  - [ ] beihilfe-thueringen-app (4 h) – „beihilfe thüringen online", Position 18, 600 Suchen
  - [ ] Nacharbeit und Prüfung (2 h)
- [ ] **Impressionen der 136 Beihilfe-Zellen gegen die Rankings legen** (6 h) – 110 von 136 ranken für kein einziges Keyword; prüfen ob tot oder nur ungeklickt
- [ ] **Zweite Messzeile in Fortschritt.base** (2 h)

## Woche 10 – Der Baukasten-Versuch und zitierfähige Fakten (40 h)

- [ ] **Ein Bundesland als Versuch zusammenlegen** (16 h) – Konkurrent hat eine Seite je Bundesland (Berlin: 249 Besucher), unser System aus 136 Seiten bringt insgesamt nur 112
  - [ ] Die acht Zellen eines Landes sichten und zusammenführen (5 h) – Bemessungssätze, ambulant, stationär, Pflege, Zahn, Beihilfestelle, App, Hub
  - [ ] Eine vollständige Seite bauen (8 h) – Vorbild: `/beihilfe/beihilfe-berlin/` beim Konkurrenten
  - [ ] Weiterleitungen setzen, interne Links nachziehen (3 h)
- [ ] **Beihilfesätze und Fristen zitierfähig machen** (12 h) – KI-Antworten zitieren klare Zahlen, keine versteckten Absätze
  - [ ] Je Bundesland die Zahlen als eigene klare Aussage (8 h) – mit Quelle und Stand
  - [ ] Einheitliches Format über alle Seiten (4 h)
- [ ] **Klären, warum ChatGPT nur einmal zitiert** (6 h) – Perplexity zitiert 30x, ChatGPT nur 1x, technisch nichts gesperrt
- [ ] **Kontaktdaten und Autorenprofile auf allen Ratgeberseiten prüfen** (6 h)

## Woche 11 – Eigene Daten, erster Teil (40 h)

- [ ] **Die Auswertung bauen** (12 h) – einziger Vorsprung, den niemand kopieren kann (30 Jahre Bestandsdaten)
  - [ ] Rohdaten aus PW ziehen und anonymisieren (5 h) – kein Einzelfall darf erkennbar sein
  - [ ] Quoten je Vorerkrankung rechnen (4 h)
  - [ ] Darstellungsformat festlegen (3 h) – einmal für alle 15 Seiten
- [ ] **Sieben PKV-Vorerkrankungsseiten mit eigenen Zahlen ergänzen** (28 h) – beste Ø-Position aller Seiten (7,33), nach Textüberarbeitung im Februar +248 % ohne die Zahlen
  - [ ] PKV mit Hashimoto (4 h)
  - [ ] PKV mit Übergewicht (4 h)
  - [ ] PKV mit Asthma (4 h)
  - [ ] PKV mit Migräne (4 h)
  - [ ] PKV mit Heuschnupfen (4 h)
  - [ ] PKV mit Corona (4 h)
  - [ ] PKV mit Brustimplantaten (4 h)

## Woche 12 – Eigene Daten, zweiter Teil (34 h)

- [ ] **Acht BU-Seiten mit eigenen Zahlen ergänzen** (32 h) – Effekt evtl. größer, da BU-Seiten heute schlechter stehen als PKV-Seiten
  - [ ] BU mit Psychotherapie (4 h) – stärkster Fall, kaum jemand schreibt ehrlich darüber
  - [ ] BU mit Hashimoto (4 h)
  - [ ] BU mit Tinnitus (4 h)
  - [ ] BU mit Morbus Crohn (4 h)
  - [ ] BU mit Migräne (4 h)
  - [ ] BU mit Übergewicht (4 h)
  - [ ] BU mit Asthma (4 h)
  - [ ] BU mit Cannabis (4 h)
- [ ] **Dritte Messzeile in Fortschritt.base** (2 h)

## Woche 13 – Hygiene und offene Fragen (40 h)

- [ ] **Slash-Dubletten auflösen** (4 h) – dieselbe Seite rankt mit/ohne Schrägstrich, nimmt sich gegenseitig Kraft
- [ ] **Uneinheitliche Slugs im Beihilfe-Baukasten vereinheitlichen** (8 h) – z. B. „nrw" vs. „nordrhein-westfalen", ä/ae uneinheitlich
- [ ] **273 interne Links auf Weiterleitungen umbiegen** (10 h)
- [ ] **Beitragserhöhungsseiten je Gesellschaft zusammenführen** (8 h) – Barmenia 2020, Concordia 2020, Debeka 2021 noch online (Abwertungsgrund)
- [ ] **Über „PKV-Zusatztarife für GKV" entscheiden** (3 h) – Position 70, 0 Klicks, 175 Impressionen: aufwerten oder zusammenlegen
- [ ] **optinvest-beamte.de auseinandernehmen** (6 h) – einzige Konkurrenzdomain, die seit einem Jahr nicht fällt, während alle anderen 41–73 % verloren haben
  - [ ] Prüfen, ob die Berufsgruppen-Achse zusätzlich trägt (3 h) – er baut nach Berufsgruppe × Sparte, wir nach Thema × Bundesland
  - [ ] Eine Zelle inhaltlich ansehen (3 h) – Rechner, eigene Zahlen oder nur Text?
- [ ] **Vierte Messzeile in Fortschritt.base** (1 h)

## Parallelspur – läuft ab Woche 1 nebenher, nicht am Ende

Diese drei Punkte sind in den Wochenstunden oben **nicht enthalten**. Wenn sie erst nach den schnellen Hebeln beginnen, fehlen sie in 12 Monaten:

- [ ] **Reputation in der Fachpresse aufbauen** – 2 h/Woche, ab Woche 1. AssCompact, VersicherungsJournal usw. Langsamster Hebel, braucht Monate bis Jahre – deshalb sofort starten.
- [ ] **Markenbekanntheit über Reichweitenarbeit** – laufend, ab Woche 1. Markensuchen sind der einzige gewachsene Bereich (+68 %, Klickrate verdoppelt). Das nimmt weder KI-Antwort noch Wettbewerber weg.
- [ ] **Monatliche Messung am 5.** – 2 h/Monat. Zahlen holen, Messzeile in [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Fortschritt.base|Fortschritt.base]] anlegen, Base prüfen. Deckt sich mit dem in [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Los-Schmerz-Wochos.md|Los-Schmerz-Wochos]] festgelegten Turnus (monatlich messen, quartalsweise entscheiden).

## Bezug zu bestehenden Notizen

- Erledigt sich teilweise mit unseren offenen Punkten in [[02 Projekte/Fairbeamtet/Los-Schmerz-Wochos/Los-Schmerz-Wochos.md|Los-Schmerz-Wochos]]: Brand Radar (Woche 1), GA4 Key Event (Woche 1) und Rank-Tracker-Erweiterung (Woche 1) sind dort schon als offene Punkte gelistet – dieser Plan liefert jetzt die konkrete Stundenschätzung und Schritt-für-Schritt-Anleitung dazu.
- Inhaltliche Themenlücken (Beihilfeergänzungstarif, Öffnungsaktion/-klausel PKV, Ruhegehalt bei Dienstunfähigkeit, Vorerkrankungsseiten) ergänzen [[02 Projekte/Fairbeamtet/Content-Erstellung.md|Content-Erstellung]].
- Wettbewerbsbeobachtung (optinvest-beamte.de, beamtenberater.com, beamtencircle.de) ergänzt [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]].
