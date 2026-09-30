---
tags:
  - ressource
  - seo
date: 2026-09-27
---

# Spam-Richtlinien und Spam-Risiko

Svens drei Fragen vom 27.09.2026, beantwortet gegen die Primärquelle **und** gegen die echten Zahlen von fairbeamtet.de. Gehört thematisch zu [[Googles No. 1]] und greift Hebel 8 vor.

## Die kurze Antwort

**1. Google ordnet fairbeamtet.de nicht als Spam ein.** Bestätigt: Sven hat am 27.09.2026 in der Search Console nachgesehen — **keine manuelle Maßnahme, keine Sicherheitsprobleme.** Die Messwerte sagen das Gegenteil: 266 von 278 Seiten sind indexiert, und die durchschnittliche Position hat sich im Jahresvergleich von 13,05 auf 9,68 **verbessert**. Eine Seite in der Spam-Schublade verliert Positionen, sie gewinnt keine.

**2. Es gibt nichts, wo man rausmuss.** Der Rückgang ist real, aber er hat ein anderes Muster — dazu unten der Abschnitt mit den Zahlen.

**3. Das einzige echte Risiko ist der Bundesland-Baukasten.** 136 der 218 Beiträge (62 %) sind Schablonen nach Ländern, einige davon mit unter 50 Wörtern eigenem Inhalt. Das ist noch kein Verstoß, aber es ist genau das Muster, das Google unter „Doorway abuse" und „Scaled content abuse" beschreibt. Da liegt die Arbeit.

## Was Google überhaupt als Spam bezeichnet

Aus den Spam-Richtlinien für die Google-Websuche, **Stand 28.08.2026**:

> „In the context of Google Search, spam refers to techniques used to deceive users or manipulate our Search systems into featuring content prominently."

Das Wort, auf das es ankommt, ist **manipulieren**. Keine der 16 Richtlinien bestraft dünnen oder mittelmäßigen Inhalt an sich. Bestraft wird die Absicht, das Ranking zu erschleichen. Wer das im Kopf behält, muss sich vor den meisten Punkten nicht fürchten.

Wie Google vorgeht:

> „We detect policy-violating practices both through automated systems and, as needed, human review that can result in a manual action. Sites that violate our policies may rank lower in results or not appear in results at all."

Zwei Wege also — Algorithmus oder Mensch. Der Unterschied ist für Frage 2 entscheidend.

### Die 16 Richtlinien und was davon uns angeht

| Richtlinie | Betrifft fairbeamtet.de? |
|---|---|
| Cloaking | Nein |
| **Doorway abuse** | **Ja, das reale Risiko** |
| Expired domain abuse | Nein |
| Hacked content | Nur bei Sicherheitslücke — WordPress-Thema, gehört zu Hebel 8 |
| Hidden text and link abuse | Nein, aber bei Akkordeons und Tabs im Page-Builder einmal prüfen |
| Keyword stuffing | Grenzwertig — siehe unten |
| Link spam | Relevant, sobald Digital PR startet ([[Digital PR und qualitative Autoritaet]]) |
| Machine-generated traffic | Nein |
| Malicious practices | Nein |
| Misleading functionality | Nein — der Beitragsrechner muss aber liefern, was er verspricht |
| **Scaled content abuse** | **Ja, das zweite reale Risiko** |
| Scraping | Nein, solange Beihilfetexte nicht aus Verordnungen abgeschrieben sind |
| Site reputation policy | Nein, kein Fremdcontent auf der Domain |
| Sneaky redirects | Nein |
| Thin affiliation | Formal nein — der Gedanke dahinter trifft uns trotzdem, siehe unten |
| User-generated spam | Nein, keine offenen Kommentare oder Foren |

## Die drei Richtlinien, die wirklich zählen

### Doorway abuse

Der Wortlaut:

> „Doorway abuse is when sites or pages are created to rank for specific, similar search queries. They lead users to intermediate pages that aren't as useful as the final destination."

Die Beispiele, und das dritte und vierte sind die, um die es geht:

> - „Having multiple websites with slight variations to the URL and home page to maximize their reach for any specific query"
> - **„Having multiple domain names or pages targeted at specific regions or cities that funnel users to one page"**
> - „Generating pages to funnel visitors into the actual usable or relevant portion of a site"
> - **„Creating substantially similar pages that are closer to search results than a clearly defined, browseable hierarchy"**

**Warum das bei uns anschlägt.** Acht Themenfamilien mal 17 Gebietskörperschaften (16 Länder plus Bund):

| Familie | Seiten |
|---|--:|
| `beihilfestelle-<land>` | 17 |
| `beihilfebemessungssatz-<land>` | 17 |
| `ambulante-leistungen-beihilfe-<land>` | 17 |
| `stationaere-leistungen-beihilfe-<land>` | 17 |
| `zahnaerztliche-leistungen-beihilfe-<land>` | 17 |
| `pflegeleistungen-beihilfe-<land>` | 17 |
| `beihilfe-<land>-app` | 17 |
| `beihilfe-<land>` bzw. `-uebersicht` | 17 |
| **Summe** | **136 von 218 Beiträgen** |

**Und warum es trotzdem kein Verstoß ist.** Der entscheidende Halbsatz lautet „targeted at specific regions **that funnel users to one page**". Unsere Landesseiten führen nicht alle auf dieselbe Zielseite, und der Inhalt unterscheidet sich sachlich: Beihilferecht ist Landesrecht, der Bemessungssatz in Bayern ist ein anderer als in Hessen, die Beihilfestelle ist eine andere Behörde. **Wer echte Landesunterschiede abbildet, betreibt keine Doorway-Seiten.** Das ist die Verteidigungslinie, und sie trägt — solange sie stimmt.

**Wo sie nicht mehr trägt.** Ich habe Bayern gegen Hessen gemessen, Navigation und Fußzeile herausgerechnet und die Landesnamen neutralisiert, damit nur echte Inhaltsunterschiede zählen:

| Seitenpaar | Rumpftext | davon wortgleich |
|---|--:|--:|
| `beihilfebemessungssatz-*` | 288 / 374 Wörter | **70,2 %** |
| `beihilfe-*-app` | 47 / 37 Wörter | 49,3 % |
| `ambulante-leistungen-beihilfe-*` | 132 / 137 Wörter | 30,8 % |
| `beihilfestelle-*` | 81 / 75 Wörter | 28,2 % |

Zwei Befunde stecken darin, und sie sind unterschiedlich schlimm.

Die Ähnlichkeit ist **nicht** das Problem. 28 bis 70 % Deckung ist für Seiten, die dieselbe Frage für ein anderes Bundesland beantworten, normal und sogar sinnvoll — die Erklärung „was ist ein Bemessungssatz" muss überall dieselbe sein.

Das Problem ist die **Menge an eigenem Inhalt**. 37 bis 374 Wörter Rumpftext. Bei den App-Seiten sind es rund 40 Wörter. Siebzehnmal. Zum Vergleich: die Hub-Seite `/private-krankenversicherung/beamte/` hat 4.531 Wörter, ein normaler Ratgeberbeitrag rund 2.900. Selbst die Beihilfe-Hub-Seite `/beihilfe/` kommt nur auf 441 Wörter — ein dünner Kopf für einen Cluster aus 136 Seiten.

### Scaled content abuse

> „Scaled content abuse is when many pages are generated for the primary purpose of manipulating search rankings and not helping users. This abusive practice is typically focused on creating large amounts of unoriginal content that provides little to no value to users, **no matter how it's created**."

Der Nachsatz ist wichtig und wird ständig falsch zitiert: **„no matter how it's created" heißt, dass KI-Erzeugung für sich genommen egal ist.** Google bestraft nicht das Werkzeug, sondern das Ergebnis. Ein von Hand getipptes 40-Wörter-Template ist genauso betroffen wie ein generiertes.

Einschlägiges Beispiel aus der Liste:

> „Creating many pages where the content makes little or no sense to a reader but contains search keywords"

Darunter fallen unsere Seiten nicht — sie ergeben Sinn. Aber der Abstand ist kleiner, als er sein müsste.

### Keyword stuffing — der Grenzfall

Ein Beispiel aus Googles Liste trifft uns beinahe:

> „Blocks of text that list cities and regions that a web page is trying to rank for"

Jede Seite der Website trägt im Menü die vollständige Liste aller 16 Länder plus Bund, und zwar **zweimal** (Desktop- und Mobilmenü sind beide im HTML). Das sind rund 450 Wörter Navigation auf einer Seite mit 40 bis 370 Wörtern Inhalt — die Navigation ist auf diesen Seiten **länger als der Text**.

Das ist kein Keyword Stuffing, weil es echte Navigation ist und keine Textblöcke. Aber es ist genau die Konstellation, in der Googles Bewertung von Supplementary Content kippt (siehe [[Interne Verlinkung und Informationsarchitektur]]): SC „can help a page better achieve its purpose **or it can detract from the overall experience**".

### Thin affiliation — formal nein, inhaltlich ja

Wir haben keine Affiliate-Links. Trotzdem lohnt der Blick, weil Google hier ausnahmsweise sagt, was **gut** ist:

> „Not every site that participates in an affiliate program is a thin affiliate. Good affiliate sites add value by offering meaningful content or features. Examples of good affiliate pages include offering additional information about price, original product reviews, rigorous testing and ratings, navigation of products or categories, and product comparisons."

Übersetzt auf einen Makler, der von Courtage lebt: **eigener Preisvergleich, eigene Tarifbewertung, echte Tests, saubere Kategorienavigation.** Das ist die Positivliste für Hebel 4 ([[Originaere Daten Tools und Experience]]) — von Google selbst formuliert, nur im Affiliate-Kapitel versteckt.

## Der Befund an den Zahlen

### Indexierung — unauffällig

Aus der Search Console, Stand 27.09.2026:

| Status | Seiten |
|---|--:|
| Submitted and indexed | 266 |
| Discovered – currently not indexed | 5 |
| Page with redirect | 2 |
| Excluded by `noindex` tag | 2 |
| Crawled – currently not indexed | 2 |
| URL is unknown to Google | 1 |
| **Gesamt** | **278** |

**95,7 % indexiert.** Eine Seite, die Google als dünn oder wertlos einstuft, sammelt „Crawled – currently not indexed" im Dutzend. Wir haben zwei. Das ist der deutlichste Einzelbeleg dafür, dass kein Qualitätsproblem auf Seitenebene vorliegt.

Drei Seiten wurden seit über 90 Tagen nicht gecrawlt und gelten damit als abstiegsgefährdet: `pflegeleistungen-beihilfe-rheinland-pfalz`, `pkv-beratung-kinder`, `beihilfebemessungssatz-berlin`.

### Sichtbarkeit — der Rückgang ist echt, aber kein Spam-Muster

| Quartal | Klicks | Impressionen | Ø Position | CTR |
|---|--:|--:|--:|--:|
| Q4 2024 | 23.055 | 911.456 | 18,18 | 2,53 % |
| Q1 2025 | 8.361 | 350.640 | 16,18 | 2,38 % |
| Q2 2025 | 14.947 | 1.005.362 | 18,31 | 1,49 % |
| Q3 2025 | 28.079 | 1.741.137 | 13,05 | 1,61 % |
| Q4 2025 | 32.031 | 1.995.147 | 8,70 | 1,61 % |
| Q1 2026 | 29.090 | 1.854.508 | 8,59 | 1,57 % |
| Q2 2026 | 22.531 | 1.278.547 | 9,37 | 1,76 % |
| Q3 2026 (bis 24.09.) | 16.352 | 871.814 | 9,68 | 1,88 % |

Q1 2025 hat eine Datenlücke (Februar fehlt), der Wert taugt nicht zum Vergleich. Q3 2026 ist noch nicht zu Ende.

**Jahresvergleich Q3 2025 zu Q3 2026**, damit die Saison herausfällt — PKV-Themen laufen im Winter, nicht im Sommer:

| | Q3 2025 | Q3 2026 | Veränderung |
|---|--:|--:|--:|
| Klicks | 28.079 | 16.352 | **−42 %** |
| Impressionen | 1.741.137 | 871.814 | **−50 %** |
| Ø Position | 13,05 | 9,68 | **3,4 Plätze besser** |
| CTR | 1,61 % | 1,88 % | **+17 %** |

**Das ist kein Abstrafungsmuster.** Eine Abstrafung sieht so aus: Position stürzt ab, Impressionen folgen. Hier ist es umgekehrt — die Position ist **besser** geworden, die CTR **höher**, und trotzdem halbieren sich die Impressionen.

Was bleibt, wenn eine Seite besser rankt und trotzdem seltener gezeigt wird: Es gibt **weniger Suchanfragen, bei denen sie überhaupt erscheint.** Die Long-Tail-Abfragen, auf denen sie bisher auf Position 30 mitlief, liefern sie nicht mehr aus. Das ist das Muster, das seit 2025 überall beschrieben wird, wo AI Overviews die Ergebnisseite besetzen. **Belegt ist hier nur die Zahlenbewegung, nicht die Ursache** — für die Ursache bräuchte es einen Abgleich, welche Abfragen weggefallen sind.

Die steigende CTR passt dazu: Wer noch kommt, kommt gezielter.

**Nachtrag vom 30.09.2026: der Zeitpunkt ist jetzt bekannt.** Die Monatswerte aus der Search Console zeigen den Bruch zwischen **Februar und März 2026** — Klicks −21 %, Impressionen −16 %, und ab da fallen die Impressionen jeden Monat weiter. Der Relaunch war am 16.01.2026, im März lief ein Core Update, und der stärkste Mitbewerber verliert im selben Monat ohne Relaunch. Drei Kandidaten, keiner ausgeschlossen. Einzelheiten und die vollständige Zeitreihe in [[Sichtbarkeitsverlauf und Relaunch]].

**Ein eingehendes Linkspam-Muster gibt es allerdings, seit Mai 2026.** Die verweisenden Domains stiegen von 114 im April auf **774 im September**, überwiegend aus `.shop`- und `.site`-Linkfarmen, fast durchgehend nofollow. Das Domain Rating bewegte sich dadurch von 3,7 auf 4,2, also praktisch nicht.

**Das ändert den Befund dieser Notiz nicht.** Google richtet sich gegen Linkspam, den eine Website *erzeugt*, nicht gegen solchen, den sie *empfängt* — eingehende Spamlinks werden in aller Regel schlicht ignoriert. Solange niemand ein Linkpaket gekauft hat, ist das kein Handlungsbedarf, sondern eine Beobachtung. Falls doch, ist es eine andere Lage.

## Frage 2: Raus aus der Schublade

Der wichtigste Punkt zuerst: **Es gibt zwei völlig verschiedene Fälle, und sie werden ständig verwechselt.**

### Fall A — manuelle Maßnahme

> „Google issues a manual action against a site when a human reviewer at Google has determined that pages on the site are not compliant with Google's spam policies."

Erkennbar in der Search Console unter **Sicherheit und manuelle Maßnahmen → Manuelle Maßnahmen**. Kein Rätselraten: Entweder steht dort ein grüner Haken oder eine Liste.

> „If your site has no manual actions, you'll see a green check mark and an appropriate message."

Der Weg zurück:

1. Ursache auf **allen** betroffenen Seiten beheben. Google ist hier eindeutig: „Fixing the issue on just some pages will not earn you a partial return to search results."
2. Sicherstellen, dass Google die Seiten erreicht — kein Login, keine Paywall, kein `robots.txt`-Ausschluss, kein `noindex`.
3. Im Bericht **Überprüfung beantragen**. Ein guter Antrag tut laut Google drei Dinge: „Explains the exact quality issue on your site. Describes the steps you've taken to fix the issue. Documents the outcome of your efforts."
4. Warten. „Most reconsideration reviews can take several days or weeks." Nicht nachfassen, bevor eine Entscheidung da ist.

### Fall B — algorithmisch

Kein Eintrag, keine Nachricht, kein Antrag möglich. **Es gibt keinen Überprüfungsantrag gegen eine algorithmische Bewertung.** Man behebt die Ursache, wartet auf den Recrawl und im Zweifel auf das nächste Core Update. Das dauert Monate, nicht Wochen.

### Was das für uns heißt

**Fall A ist ausgeschlossen.** Sven hat den Bericht am 27.09.2026 selbst geprüft: „Keine Probleme erkannt", ebenso unter Sicherheitsprobleme. Damit ist die Frage nicht mehr wahrscheinlich, sondern beantwortet.

**Fall B ist nach allem, was messbar ist, ebenfalls auszuschließen.** 95,7 % Indexabdeckung, zwei Seiten im Status „Crawled – currently not indexed", steigende Durchschnittsposition. Eine algorithmisch abgewertete Seite sieht anders aus.

**Es gibt also nichts, wo man rausmuss.** Die Frage „wie komme ich aus der Spam-Schublade" hat für fairbeamtet.de keinen Gegenstand. Was bleibt, ist Frage 3 — und die ist Vorbeugung, nicht Reparatur.

## Frage 3: Content so bauen, dass er gar nicht erst auffällt

Aus den Richtlinien abgeleitet, nicht erfunden. Der Maßstab ist immer derselbe: **Würde diese Seite auch existieren, wenn es Google nicht gäbe?**

**Kein Seitenmuster ohne eigenen Anlass.** Eine neue Seite entsteht, weil es zu diesem Thema etwas Eigenes zu sagen gibt — nicht, weil das Muster noch eine Lücke hat. Die Frage „welches Bundesland fehlt noch" ist die falsche Frage. Die richtige lautet: „Was ist in Sachsen-Anhalt anders, und reicht das für eine eigene Seite?"

**Untergrenze für eigenen Inhalt.** Wenn sich eine Landesseite nach Abzug von Navigation und Standarderklärung auf drei Sätze reduzieren lässt, ist sie keine Seite, sondern eine Tabellenzeile. Dann gehört sie in eine Übersichtstabelle auf der Hub-Seite. Das ist kein SEO-Trick, das ist für den Leser besser.

**Was die Seite besitzt, was sonst niemand hat.** Ein eigener Rechenweg, ein Screenshot des tatsächlichen Antragsformulars, die Bearbeitungsdauer aus der eigenen Praxis, ein Fallbeispiel aus einer echten Beratung. Genau die Liste, die Google im Affiliate-Kapitel als „adds value" aufzählt. Zu Erfahrungswissen siehe [[Originaere Daten Tools und Experience]].

**Keine Seite, die woanders besser beantwortet wird.** Wenn die Beihilfestelle Hessen die Öffnungszeiten selbst veröffentlicht, ist eine Seite, die nur diese Öffnungszeiten wiedergibt, „reproducing content feeds without providing some type of unique benefit to the user". Wert entsteht durch Einordnung, nicht durch Wiedergabe.

**KI ist erlaubt, KI-Ausschuss nicht.** „No matter how it's created" — das Werkzeug ist Google gleichgültig. Wer mit KI eine echte Recherche beschleunigt, verstößt gegen nichts. Wer siebzehn Varianten desselben Textes erzeugt, schon.

**Keine Behauptung ohne Beleg, keine Zahl ohne Quelle und Datum.** Bei einem YMYL-Thema wie Krankenversicherung ist das nicht nur Spam-Schutz, sondern der Kern von Hebel 1 ([[Trust und E-E-A-T-System]]).

**Keine Funktion versprechen, die nicht liefert.** Der Beitragsrechner muss rechnen, nicht nur ein Formular einsammeln. Sonst greift „Misleading functionality".

**Links kaufen ist tabu, Werbung kennzeichnen ist Pflicht.** Google zieht die Grenze nicht beim Bezahlen, sondern beim Weitergeben von Ranking-Kraft: gekaufte oder gesponserte Links sind zulässig, „as long as they are qualified with a `rel="nofollow"` or `rel="sponsored"` attribute value". Wichtig, sobald Digital PR anläuft.

**Navigation ist Inhalt.** Ein Menü, das auf jeder Seite alle 17 Gebietskörperschaften zweimal ausliefert, ist bei 40 Wörtern Text kein Service mehr.

## Die drei Aufräumpunkte, die dabei aufgefallen sind

Keine Aufgaben, nur Befunde — die Umsetzung gehört in die Bestandsprüfung nach den zehn Hebeln.

**Vier URLs haben kaputte Umlaut-Umschriften.** `zahnarztliche-` statt `zahnaerztliche-` (dreimal: Baden-Württemberg, Nordrhein-Westfalen, Bund) und `stationare-` statt `stationaere-` (Baden-Württemberg). Nicht schlimm fürs Ranking, aber es verrät die Schablone.

**Die Abkürzungen sind uneinheitlich.** Mal `nrw`, mal `nordrhein-westfalen`, mal `nordrhein-westfalen-nrw`; dazu `-mv`, `-rp`, `-bw` nur bei einzelnen Ländern. Innerhalb derselben Familie unterschiedlich. Erschwert jede Auswertung und jeden konsistenten Ankertext.

**Das HTML ist aufgebläht.** 310 bis 340 KB Quelltext für 550 bis 680 Wörter Text. *(Präzisiert am 27.09.2026: Über die Leitung gehen dank Brotli nur 65 bis 90 KB. Das Problem ist nicht die Übertragungsmenge, sondern dass **66 % des Dokuments nicht zwischenspeicherbarer Inline-Code** sind — allein 69,5 KB Cookie-Banner-Konfiguration je Seite. Auswertung in [[Mobile UX und Core Web Vitals]].)*

## Quellen

Überblick über alle Fachleute mit Werbe-Check: [[SEO-Fachleute und Quellen]].

**Primär:**
- [Spam policies for Google web search](https://developers.google.com/search/docs/essentials/spam-policies) — **Stand 28.08.2026**, alle 16 Richtlinien im Wortlaut
- [Manual actions report](https://support.google.com/webmasters/answer/9044175) — Definition der manuellen Maßnahme, Ablauf und Dauer der Überprüfung
- [Search Quality Rater Guidelines, 11.09.2025](https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf) — 2.4.2 zu Supplementary Content

**Eigene Messung, 27.09.2026:**
- Sitemap-Auswertung über `https://www.fairbeamtet.de/sitemap_index.xml` — 218 Beiträge, 34 Seiten, 21 Kategorien, 4 Autoren, 5 Videos, 1 Local
- Textmessung der Landesseiten Bayern gegen Hessen, Rohquelltext, Navigation und Fußzeile herausgerechnet
- Search-Console-Daten über SEO Gets, Indexstatus und Quartalswerte Q4 2024 bis Q3 2026

**Bestätigt durch Sven, 27.09.2026:**
- Search Console → Sicherheit und manuelle Maßnahmen → **Manuelle Maßnahmen: keine Probleme erkannt**
- Search Console → **Sicherheitsprobleme: keine Probleme erkannt**

**Nicht belegt:**
- Die Ursache des Impressionsrückgangs. Die Bewegung ist gemessen, die Erklärung über AI Overviews ist eine naheliegende Vermutung ohne Nachweis.

## Offene Punkte

- **Welche Abfragen sind weggefallen?** Ein Abgleich der Suchanfragen Q3 2025 gegen Q3 2026 würde zeigen, ob der Verlust im Long Tail liegt. Gehört zur Bestandsprüfung.
- **Die App-Seiten.** 17 Seiten mit rund 40 Wörtern eigenem Inhalt sind der schwächste Punkt im ganzen Bestand. Erste Kandidaten für Zusammenlegung.
- **Akkordeons und Tabs im Page-Builder** noch nicht darauf geprüft, ob Text per CSS versteckt wird. Formal wäre das „hidden text".
