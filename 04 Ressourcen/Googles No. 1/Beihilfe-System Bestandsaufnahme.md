---
tags:
  - ressource
  - seo
date: 2026-09-29
---

# Beihilfe-System Bestandsaufnahme

Struktur und Leistung des Bundesland-Baukastens, gemessen am 28./29.09.2026. Die Struktur stammt aus der Sitemap, die Leistungszahlen aus Ahrefs (Land DE, Stand 28.09.2026).

Der Baukasten war bis dahin nur als Risiko beschrieben, siehe [[Spam-Richtlinien und Spam-Risiko]]. Hier steht, was er wirklich ist und was er bringt.

## Der Aufbau ist eine Matrix

**8 Themenfamilien × 17 Beihilfevorschriften** (16 Länder plus Bund). Soll: 136 Zellen. Ist: **136, die Matrix ist vollständig.**

| Familie | Zellen |
|---|--:|
| Alle acht Familien | je 17/17 |

**Korrektur vom 30.09.2026.** Hier stand bis dahin, es fehle „Zahnärztliche Leistungen Beihilfe Thüringen" und die Seite existiere in keiner Schreibweise. **Das war falsch.** Sie existiert, trägt den richtigen Titel „Zahnärztliche Leistungen Beihilfe Thüringen", liefert HTTP 200 und steht in der Sitemap — aber unter `/zahnaerztliche-leistungen-thueringen/`, also **ohne `beihilfe` im Slug**. Die 16 anderen Zellen der Familie haben es. Geprüft am 30.09.2026 gegen `page-sitemap.xml` und `post-sitemap`.

Es ist also keine fehlende Seite, sondern ein weiterer Slug-Bruch — und ein Beleg dafür, wie schnell eine Auswertung nach Namensmuster danebengreift. Siehe den nächsten Abschnitt.

## Zwei Einstiege, beide funktionieren

Das System hat zwei Hub-Typen, und sie greifen unterschiedlich:

- **Länder-Hub** `/beihilfe-<land>/` — fasst alle acht Themen für ein Land zusammen, rund 1.200 bis 1.400 Wörter mit echten Zahlen. Verlinkt **seitwärts** zu den 16 anderen Länder-Hubs, nicht nach unten zu den eigenen Unterseiten.
- **Themen-Hub** `/beihilfe-ratgeber/<thema>/` — fasst ein Thema über alle Länder zusammen. Verlinkt **nach unten** auf alle 17 Länderzellen.

**Keine Verwaisung.** Jede Zelle hängt am Themen-Hub. Dass die Länder-Hubs ihre eigenen Unterseiten nicht verlinken, ist eine Lücke, aber kein Bruch.

## Die Slugs sind uneinheitlich

Vier Seiten schreiben ä als `a` statt als `ae` und brechen damit das Muster:

- `stationare-leistungen-beihilfe-baden-wuerttemberg`
- `zahnarztliche-leistungen-beihilfe-baden-wuerttemberg`
- `zahnarztliche-leistungen-beihilfe-bund`
- `zahnarztliche-leistungen-beihilfe-nordrhein-westfalen`

Dazu die Ländernamen selbst: NRW als `nrw`, `nordrhein-westfalen` und `nordrhein-westfalen-nrw`. Der Bund als `bund` und `bund-bundesbeihilfe`. Baden-Württemberg, Mecklenburg-Vorpommern und Rheinland-Pfalz je mit und ohne Kürzel, Niedersachsen teils mit `-uebersicht`.

Dazu die Thüringen-Zelle ohne `beihilfe` im Slug, siehe oben.

Funktional stört das nichts, die Hubs verlinken korrekt. **Aber jede Auswertung, die auf dem Muster aufbaut, zählt falsch** — diese hier hat es vorgemacht und eine vorhandene Seite als fehlend gemeldet.

## Die Leistung ist schwach

**62 % der Beiträge, 7,6 % des Traffics.**

| | Umfang | Traffic/Monat |
|---|--:|--:|
| Beihilfe-System | 135 Zellen + 9 Hubs | ≈ 112 |
| Alles andere | 83 Beiträge | ≈ 1.364 |

Einordnung:

- **Nur 68 von 283 URLs ranken überhaupt** in den Top 100.
- Von den 135 Zellen tauchen rund **25** auf. Die übrigen 110 ranken für kein einziges Keyword.
- Eine einzige Seite, `/familienzuschlag-fuer-beamte/` mit 403 Besuchern, macht das **3,6-fache des gesamten Systems**.

## Was funktioniert: die App-Seiten

Der wichtigste Befund. Die App-Familie ist mit rund 40 Wörtern die dünnste im System — und der mit Abstand beste Teil:

| Seite | Traffic | Top-Keyword | Pos. |
|---|--:|---|--:|
| beihilfe-schleswig-holstein-app | 33 | beihilfe sh app | 9 |
| beihilfe-berlin-app | 19 | beihilfe berlin app | 7 |
| beihilfe-niedersachsen-app | 8 | beihilfe app niedersachsen | 8 |
| beihilfe-sachsen-anhalt-app | 5 | beihilfe app sachsen-anhalt | 6 |
| beihilfe-thueringen-app | 5 | beihilfe thüringen online | 18 |

**71 von 112 Besuchern, also 63 % des Beihilfe-Traffics, kommen aus der App-Familie.**

Daraus folgt die Regel für den ganzen Baukasten: **Die Zelle trägt, wenn die Frage eine Antwort hat, nicht ein Thema.** „Beihilfe App Niedersachsen" ist eine Frage. „Ambulante Leistungen Beihilfe Bayern" ist ein Thema — und rankt nicht. Die inhaltsstärksten Familien, Bemessungssätze und Leistungen, sind fast unsichtbar.

**Eine fremde Einschätzung sagt dasselbe.** Cyrus Shepard sortiert Inhaltsarten nach Haltbarkeit, siehe [[Content-Typen im Zero-Click-Zeitalter]]. „Ratgeber und Erklärstücke" stuft er als **schwach** ein, „Verzeichnisse und Datenbanken" als mittel — letztere aber nur, wenn sie eigene Erstdaten und echte Aktualität mitbringen. In dieser Sprache gelesen sind die App-Seiten ein Verzeichniseintrag mit Aufgabenerledigung, die Themenseiten dagegen Ratgeber. Die Messung oben und diese Einstufung sind unabhängig voneinander entstanden und zeigen in dieselbe Richtung. **Das ist keine Ursache, sondern eine Arbeitshypothese** — aber sie schärft die Frage für den nächsten Schritt: Lässt sich je Bundesland genug Eigenes beibringen, um aus der Schablone ein Verzeichnis zu machen? Wenn nein, ist Zusammenlegen die ehrlichere Antwort.

## Wo der Hebel liegt

Nicht in neuen Seiten. In fünf, die knapp danebenstehen:

| Seite | Keyword | Pos. | Volumen |
|---|---|--:|--:|
| beihilfestelle-berlin | landesverwaltungsamt berlin beihilfe | 24 | 800 |
| beihilfe-thueringen-app | beihilfe thüringen online | 18 | 600 |
| beihilfestelle-hessen | beihilfe kassel | 18 | 600 |
| beihilfestelle-hessen | beihilfestelle hessen | 20 | 500 |
| beihilfe-berlin | beihilfe berlin pensionäre | 13 | 600 |

Zusammen **3.100 Suchanfragen im Monat**, alle außerhalb der Top 10. Fünf Seiten auf Seite 1 zu schieben bringt mehr als zwanzig neue anzulegen.

## Nebenbefund: Slash-Dubletten

Mehrere Seiten ranken doppelt, mit und ohne abschließenden Slash: `/amtsaerztliche-untersuchung/` (110 Besucher) gegen `/amtsaerztliche-untersuchung` (9), dazu `beihilfe-hamburg`, `beihilfestelle-hessen`, `beihilfestelle-niedersachsen` und `debeka-dbv-oder-huk`. Dieselbe Seite unter zwei Adressen, die sich gegenseitig Signale nehmen. Gehört zu [[Technische Indexhygiene]].

## Was diese Zahlen nicht sagen

**GEO ist nicht gemessen.** Die Struktur ist ausdrücklich auch für KI-Antworten gebaut. Organischer Traffic bildet das nicht ab. Laut [[SERP AI und Conversion-Optimierung]] zitiert Perplexity fairbeamtet dreißigmal, ChatGPT einmal. Für den GEO-Teil braucht es Brand Radar oder AI-Zitationsdaten.

**Ahrefs schätzt.** Bei deutschem Longtail ist der Index dünn. Erst der Abgleich mit den Impressionen aus der Search Console zeigt, ob die 110 stummen Zellen wirklich tot sind oder nur nie geklickt werden. **Das ist der nächste Schritt.**

## Herleitung
- Struktur: [sitemap_index.xml](https://www.fairbeamtet.de/sitemap_index.xml), 283 URLs, gezählt am 29.09.2026
- Leistung: Ahrefs Site Explorer, Top Pages, Land DE, Stand 28.09.2026
- Der Baukasten als Spam-Risiko: [[Spam-Richtlinien und Spam-Risiko]]
- Was stattdessen gebaut werden sollte: [[Content-Roadmap 2027]]
- Kannibalisierung zwischen Hub und Zelle: [[Topical Authority ohne Kannibalisierung]]
