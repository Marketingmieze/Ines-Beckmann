---
tags: [projekt, fairbeamtet]
status: entwurf
erstellt: 2026-11-13
---

# Familienzuschlag-Rechner (fairbeamtet.de)

## Ziel

Ein eigenständiger Familienzuschlag-Rechner für fairbeamtet.de, nach demselben Muster wie [[02 Projekte/Fairbeamtet/BMI-Rechner.md|BMI-Rechner]]: ein fokussiertes, eigenständig funktionierendes Tool statt des großen, noch nicht freigegebenen Beihilfe-/PKV-Lückenrechners aus [[02 Projekte/Fairbeamtet/Eigener Gehaltsrechner.md|Eigener Gehaltsrechner – Analyse & Konzept]].

Direkter Bezug zur Konkurrenzanalyse dort: Der Gehaltsrechner von einfachverbeamtet.de bringt laut [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]] rund ein Viertel des gesamten Konkurrenz-Traffics, und der Familienzuschlag ist einer der Eingabe-/Ausgabe-Bausteine dort. Eigene fairbeamtet.de-Seite zum Thema existiert bereits ([Familienzuschlag für Beamte: Höhe und Anspruch 2026](https://www.fairbeamtet.de/familienzuschlag-fuer-beamte/)), aber **ohne Rechner** – nur Text, Tabellen und zwei Beispielrechnungen. Dieses Tool löst das ein.

## Status

**Entwurf – noch nicht mit Sven abgestimmt.** Die Datenlage hat sich gegenüber der ersten Version grundlegend verbessert: Fast alle Zahlen sind jetzt gegen **offizielle Besoldungstabellen des dbb (Deutscher Beamtenbund und Tarifunion)** geprüft, nicht mehr gegen Sekundärquellen-Aggregatoren. Zwei Einschränkungen bleiben:
1. Mehrere dbb-Tabellen (Baden-Württemberg, Bayern, Bremen, u. a.) tragen den Vermerk **„Entwurf – Veröffentlichung unter Vorbehalt der Bekanntmachung im Gesetzblatt"** – die Zahlen stammen aus dem Gesetzgebungsverfahren, sind aber zum Abrufzeitpunkt (13.11.2026) noch nicht formal im jeweiligen Gesetzblatt verkündet. Hohe Wahrscheinlichkeit, dass sie final so gelten, aber kein Ersatz für eine Gesetzblatt-Prüfung vor Launch.
2. Thüringen: keine dbb-Tabelle für 2026 gefunden, nur Stand 1. Februar 2025.

**Vor Veröffentlichung weiterhin empfohlen:** kurzer Abgleich der "Entwurf"-Länder gegen die zwischenzeitlich verkündeten Gesetzblätter, analog zur Vorgabe beim BMI-Rechner (Rangfolge Voice Profile Punkt 1: fachliche Richtigkeit schlägt alles andere).

## Rechtliche Grundlage

Bundesbeamte: § 40 BBesG. Landesbeamte: seit der Föderalismusreform 2006 die jeweiligen 16 Landesbesoldungsgesetze (eigene Anlagen zum Familienzuschlag, nicht mehr bundeseinheitlich). Das ist auch der Grund, warum die Struktur zwischen den Ländern so stark variiert (manche ganz ohne „Stufe 1", manche mit Besoldungsgruppen- oder Ortsklassen-/Mietenstufen-Abhängigkeit).

## Recherche: Familienzuschlag nach Bundesland – vollständige Daten (Primärquelle: dbb-Besoldungstabellen, Stand der Recherche: 13.11.2026)

Komplett neu recherchiert über die offiziellen Besoldungstabellen des dbb ([dbb.de/beamtinnen-beamte/besoldungstabellen.html](https://www.dbb.de/beamtinnen-beamte/besoldungstabellen.html)), jeweils die aktuellste 2026er-Fassung pro Bundesland heruntergeladen und direkt aus dem PDF ausgelesen (nicht per automatisiertem Seitenabruf mit kleinem Hilfsmodell, sondern mit Skript-Extraktion des PDF-Texts – das vermeidet die Rowspan-/OCR-Fehler, die bei der ersten Bayern/NRW-Recherche aufgetreten waren).

**Grundwerte (Standardfall: übrige/häufigste Besoldungsgruppe, keine Orts-/Mietenstufe):**

| Bundesland | Stufe 1 (verheiratet/verpartnert) | 1. Kind | 2. Kind | ab 3. Kind | Gültig ab | Quellenstatus |
|---|---|---|---|---|---|---|
| Bund | 181,36 € | +154,99 € (Stufe 2 gesamt: 336,35 €) | +154,99 € | +482,89 € je Kind | 01.05.2026 | final verkündet |
| Baden-Württemberg | 180,46 € | +157,78 € | +157,78 € | +989,17 € je Kind | 01.04.2026 | Entwurf |
| Bayern | 87,51 € (Ortsklasse I; s. Detailtabelle) | s. Detailtabelle (Ortsklasse I: 506,90 € Stufe 1 gesamt) | s. Detailtabelle | s. Detailtabelle | 01.10.2026 | Entwurf |
| Berlin | kein Stufe-1-Anteil | +148,44 € | +148,44 € | 3. Kind +819,76 €, ab 4. Kind +678,99 € | 01.04.2026 | final verkündet |
| Brandenburg | kein Stufe-1-Anteil | +377,16 € | +377,16 € | +888,39 € je Kind | 01.01.2026 | final verkündet |
| Bremen | 166,18 € (A5–A8) / 174,54 € (übrige) | +432,03 €/+440,39 € gesamt (Stufe 2) | +265,85 € | 3. Kind +610,60 €, ab 4. Kind +587,27 € | 01.04.2026 | Entwurf |
| Hamburg | 165,84 € | +193,14 € | +193,14 € | +635,00 € je Kind | 01.04.2026 | final verkündet |
| Hessen | 177,30 € | +360,57 € | +360,57 € | +831,08 € je Kind | 01.07.2026 | final verkündet |
| Mecklenburg-Vorpommern | 164,77 € | +198,83 € (Stufe 2 gesamt: 363,60 €) | +198,83 € | +820,00 € je Kind | 01.04.2026 | final verkündet |
| Niedersachsen | 162,26 € (A5–A8) / 170,36 € (übrige) | +145,61 € (Stufe 2 gesamt: 307,87 €/315,97 €) | +145,61 € | +512,37 € je Kind | 01.04.2026 | final verkündet |
| Nordrhein-Westfalen | 169,26 €/167,26 €/173,50 € (nach BesGr, s. Detailtabelle) | s. Detailtabelle (Mietenstufen-/BesGr-Matrix) | s. Detailtabelle | s. Detailtabelle | 01.04.2026 | final verkündet (amtliches PDF) |
| Rheinland-Pfalz | 88,03 € | +246,97 € | +246,97 € | +726,00 € je Kind, ggf. + Mietenstufen-Aufstockung | 01.04.2026 | final verkündet |
| Saarland | 164,48 € | +165,31 € (Stufe 2 gesamt: 329,79 €) | +165,31 € | +781,68 € je Kind | 01.04.2026 | final verkündet |
| Sachsen | 279,58 € | +279,58 € (Stufe 2 gesamt: 559,16 €) | +279,58 € | +795,41 € je Kind | 01.04.2026 | final verkündet |
| Sachsen-Anhalt | 169,04 € | +184,85 € (Stufe 2 gesamt: 353,89 €) | +184,85 € | +818,98 € je Kind | 01.04.2026 | final verkündet |
| Schleswig-Holstein | 176,24 € | +199,85 € (Stufe 2 gesamt: 376,09 €) | +199,85 € | +516,48 € je Kind | 01.01.2026 | final verkündet |
| Thüringen | 177,25 € | 326,41 € gesamt (1 Kind) | 529,16 € gesamt (2 Kinder) | 830,50 € gesamt (3 Kinder), ab 4. Kind jeweils +803,23 € | **01.02.2025** (keine 2026er dbb-Tabelle gefunden) | veraltet – zu prüfen |

**Wichtiger Struktur-Hinweis:** Die Spalten "1. Kind"/"2. Kind"/"ab 3. Kind" sind bei den meisten Ländern **Erhöhungen**, die auf Stufe 1 aufaddiert werden (additive Logik). Bei Bayern, NRW, Hamburg, Thüringen und teilweise Bremen sind die Werte dagegen **Gesamtbeträge je Stufe** (die Stufe selbst enthält bereits den Ehezuschlag) – in der Tabelle oben jeweils vermerkt. Das muss im Rechner-Code so unterschieden werden, sonst entstehen Doppelzählungen oder falsche Summen.

### Quellen

- [dbb.de – Besoldungstabellen (Übersicht aller Bundesländer)](https://www.dbb.de/beamtinnen-beamte/besoldungstabellen.html) – Primärquelle für fast alle Länder, jeweils aktuellste 2026er-PDF-Datei
- [recht.nrw.de – Anhang 8 LBesG NRW](https://recht.nrw.de/system/files/2026-08/lrgv_lbesg_anlage-13_stand-01.04.2026.pdf) – amtliches Original-PDF für NRW
- [gesetze-bayern.de – Anlage 5 BayBesG](https://www.gesetze-bayern.de/Content/Document/BayBesG-ANL_5) – amtlicher Gesetzestext, zeigt zum Abrufzeitpunkt noch den älteren Stand 01.02.2025 (dbb-Tabelle mit Stand 01.10.2026 ist aktueller, s. Bayern-Detailabschnitt)
- [haufe.de – Anlage 6 ThürBesG](https://www.haufe.de/id/norm/besoldungsgesetz-thueringen-anlage-6-zu-37-familienzuschlag-und-anrechnungsbetrag-HI16460882.html) – bestätigt den Feb.-2025-Stand für Thüringen unabhängig von der dbb-Tabelle

## Besoldungsgruppen-abhängige Zusatzkomponenten je Bundesland

Das ist der Teil, der für "jede Besoldungsgruppe" entscheidend ist. Mehrere Länder erhöhen den Familienzuschlag zusätzlich für niedrigere Besoldungsgruppen, oder haben komplett eigene Matrizen. Alle Werte aus den dbb-Tabellen, Stand wie oben.

### Bund – Erhöhungsbeträge A 3–A 5

Für das erste Kind in A 3–A 5 (und Anwärter des einfachen Dienstes): **+5,37 €**. Für jedes weitere Kind: A 3 +26,84 €, A 4 +21,47 €, A 5 +16,10 €.

### Baden-Württemberg – mehrstufig, komplexeste Struktur im Datensatz

- Kinderbezogener Teil erhöht sich für das **erste** Kind in A 7–A 10 um **+56,82 €**, in A 11–A 13 um **+28,41 €**.
- Zusätzlich eine **Erhöhung des kinderbezogenen Teils für das zweite Kind nach Besoldungsgruppe UND Stufe des Grundgehalts** (eigene Matrix A 7–A 14 × Erfahrungsstufe 1–10, Beträge von 5,96 € bis 511,38 €, tendenziell höher bei niedrigerer Stufe).
- Zusätzlich ein **Familienergänzungszuschlag** (separate Matrix "Betrag, den eine Familie mit einem Kind insgesamt erhält" bzw. "mit mindestens zwei Kindern", nach BesGr A 7–A 10 × Stufe, bis zu 790 € bei einem Kind bzw. 989,17 € bei Familienergänzungszuschlag nach Stufe-Werten).
- **Einordnung:** Baden-Württemberg ist das einzige Bundesland im Datensatz, bei dem der Betrag nicht nur von Besoldungsgruppe, sondern zusätzlich von der **Erfahrungsstufe des Grundgehalts** abhängt. Für eine vollständig korrekte Abbildung bräuchte der Rechner ein zusätzliches Eingabefeld "Erfahrungsstufe", nur für Baden-Württemberg.

### Bayern – aktualisierte Primärquelle (dbb, gültig ab 1. Oktober 2026 – neuer als gesetze-bayern.de)

Die dbb-Tabelle zeigt einen **neueren Stand (01.10.2026)** als der amtliche Gesetzestext auf gesetze-bayern.de, der beim ersten Abruf noch "01.02.2025" zeigte. Korrekt rekonstruiert (gleiche Rowspan-Logik wie beim Februar-2025-Stand, Werte jetzt höher):

| Ortsklasse | Stufe L (ledig) | Stufe V (verheiratet) | Stufe 1 (1 Kind, gesamt) | Stufe 2 (2 Kinder, gesamt) | zzgl. 3. Kind | zzgl. jedes weitere Kind |
|---|---|---|---|---|---|---|
| I | – | 87,51 € | 346,98 € | 506,90 € | 495,64 € | 593,37 € |
| II | – | 87,51 € | 346,98 € | 506,90 € | 495,64 € | 593,37 € |
| III | – | 87,51 € | 346,98 € | 542,58 € | 510,51 € | 640,81 € |
| IV | – | 87,51 € | 370,73 € | 578,24 € | 525,84 € | 688,72 € |
| V | – | 112,50 € | 394,46 € | 613,90 € | 541,61 € | 737,05 € |
| VI | – | 137,50 € | 418,20 € | 693,03 € | 557,87 € | 785,88 € |
| VII | 170,26 € | 170,26 € | 546,06 € | 784,86 € | 574,59 € | 835,19 € |

**Erhöhungsbeträge A 3–A 10** (gültig ab 1. Oktober 2026, je Ortsklasse, ab Stufe 1 für jedes Kind):

| Ortsklasse | A 3 | A 4 | A 5 | A 6 | A 7 | A 8 | A 9 | A 10 |
|---|---|---|---|---|---|---|---|---|
| I | 35,15 € | 31,12 € | 30,05 € | 27,96 € | 24,59 € | 22,34 € | 18,09 € | 10,91 € |
| II | 37,26 € | 34,96 € | 33,76 € | 31,40 € | 27,63 € | 25,09 € | 20,31 € | 12,25 € |
| III | 41,40 € | 38,85 € | 37,51 € | 34,88 € | 30,70 € | 27,87 € | 22,55 € | 13,60 € |
| IV | 45,99 € | 43,15 € | 41,67 € | 38,73 € | 34,11 € | 30,97 € | 25,06 € | 15,11 € |
| V | 50,54 € | 47,41 € | 45,79 € | 42,57 € | 37,47 € | 34,03 € | 27,52 € | 16,61 € |
| VI | 54,92 € | 51,52 € | 49,75 € | 46,27 € | 40,72 € | 36,97 € | 29,91 € | 18,06 € |
| VII | 60,35 € | 56,61 € | 54,68 € | 50,83 € | 44,74 € | 40,62 € | 32,87 € | 19,83 € |

### Berlin – Ergänzender Familienzuschlag nach § 40a BBesG BE

Zusätzlich zum regulären Zuschlag (§ 40) gibt es einen **Ergänzenden Familienzuschlag** für Fälle, in denen der reguläre Zuschlag nicht oder nur reduziert gewährt wird: ohne Kind 176,44 €, für ein Kind 638,81 €, für zwei Kinder 718,65 €. Komplexer Sonderfall (betrifft primär Teilzeit-/Mischkonstellationen) – im MVP-Rechner nicht abgebildet, nur als Hinweis im Ergebnis.

### Bremen – zweistufig nach Besoldungsgruppenband, plus Familienergänzungszuschlag

- Stufe 1/Stufe 2 (A 5–A 8 bzw. übrige) siehe Grundtabelle oben.
- Erhöhung in A 5: Stufe 2 für das erste Kind +18,00 €, ab Stufe 3 für jedes weitere Kind +40,00 €.
- **Familienergänzungszuschlag** (§ 35a BremBesG, zusätzlich zum klassischen Zuschlag): 1. Kind 375,00 €, 2. Kind 375,00 €, 3. Kind 375,00 €, 4. und jedes weitere Kind 385,00 €.

### Mecklenburg-Vorpommern – Erhöhungsbeträge A 4–A 6

Für das erste und zweite Kind in den Stufen 2 und 3: A 4 +36,17 €, A 5 +31,17 €, A 6 +16,17 €.

### Niedersachsen – Laufbahngruppe 1

In der Laufbahngruppe 1, Besoldungsgruppen A 5–A 9, erhöht sich der Zuschlag in den Stufen 2 und 3 für jedes Kind um **+100,00 €**.

### Nordrhein-Westfalen – vollständige Mietenstufen-/Besoldungsgruppen-Matrix

Direkt aus dem amtlichen PDF [recht.nrw.de](https://recht.nrw.de/system/files/2026-08/lrgv_lbesg_anlage-13_stand-01.04.2026.pdf), gültig ab 1. April 2026.

**Stufe 1 (Ehezuschlag, unabhängig von Mietenstufe):**

| Besoldungsgruppe | Betrag |
|---|---|
| A 5 und A 6 | 169,26 € |
| A 7 und A 8 | 167,26 € |
| übrige (ab A 9) | 173,50 € |

**Stufe 2–5 (Gesamtbetrag inkl. Ehezuschlag, nach Mietenstufe I–VII):**

| Stufe | BesGr | I | II | III | IV | V | VI | VII |
|---|---|---|---|---|---|---|---|---|
| Stufe 2 (1 Kind) | A5/A6 | 323,89 € | 323,89 € | 373,17 € | 518,14 € | 650,94 € | 793,75 € | 954,44 € |
| | A7/A8 | 320,07 € | 320,07 € | 369,36 € | 514,32 € | 647,13 € | 769,94 € | 950,62 € |
| | übrige | 324,52 € | 324,52 € | 373,81 € | 518,76 € | 651,57 € | 794,39 € | 955,05 € |
| Stufe 3 (2 Kinder) | A5/A6 | 737,09 € | 880,30 € | 1.027,88 € | 1.199,36 € | 1.361,94 € | 1.529,08 € | 1.724,50 € |
| | A7/A8 | 731,44 € | 874,66 € | 1.022,24 € | 1.193,72 € | 1.356,29 € | 1.523,45 € | 1.718,87 € |
| | übrige | 734,08 € | 877,30 € | 1.024,87 € | 1.196,36 € | 1.358,93 € | 1.526,09 € | 1.721,50 € |
| Stufe 4 (3 Kinder) | A5/A6 | 1.450,50 € | 1.615,85 € | 1.789,38 € | 1.991,40 € | 2.176,88 € | 2.373,13 € | 2.600,78 € |
| | A7/A8 | 1.439,21 € | 1.604,55 € | 1.778,08 € | 1.980,11 € | 2.165,58 € | 2.361,84 € | 2.588,49 € |
| | übrige | 1.436,24 € | 1.601,59 € | 1.775,12 € | 1.977,14 € | 2.162,61 € | 2.358,88 € | 2.586,52 € |
| Stufe 5 (4 Kinder) | A5/A6 | 2.169,15 € | 2.359,21 € | 2.559,84 € | 2.789,90 € | 2.999,21 € | 3.237,91 € | 3.498,95 € |
| | A7/A8 | 2.152,20 € | 2.342,26 € | 2.542,88 € | 2.772,95 € | 2.982,26 € | 3.220,96 € | 3.482,00 € |
| | übrige | 2.143,84 € | 2.333,59 € | 2.534,32 € | 2.784,39 € | 2.973,69 € | 3.212,40 € | 3.473,44 € |
| ab 5. Kind, je Kind | A5/A6 | 760,89 € | 788,82 € | 819,69 € | 851,89 € | 879,53 € | 928,98 € | 968,42 € |
| | A7/A8 | 755,23 € | 783,16 € | 814,02 € | 846,23 € | 873,87 € | 923,32 € | 962,70 € |
| | übrige | 749,64 € | 777,56 € | 808,43 € | 840,64 € | 868,27 € | 917,73 € | 957,16 € |

Zusätzlich in A 5: Stufe 2 für das erste Kind +8,65 €, ab Stufe 3 für jedes weitere Kind +25,67 €.

**Wichtig für die Implementierung:** NRW rechnet nicht additiv (Ehezuschlag + x € pro Kind), sondern gibt für jede Kinderzahl einen eigenen Gesamtbetrag pro Mietenstufe und Besoldungsgruppenband aus. Der Rechner-Code muss das als dreidimensionale Lookup-Tabelle (Besoldungsgruppenband × Mietenstufe × Kinderzahl) abbilden.

### Rheinland-Pfalz – Erhöhung A 5 plus mietenstufenabhängige Aufstockung

- Erhöhung in A 5: für das erste Kind +5,32 €, für das zweite Kind +15,98 €.
- **Mietenstufenabhängige Aufstockung** für das dritte und jedes weitere Kind: Mietenstufe V +19,00 €, Mietenstufe VI +43,00 €, Mietenstufe VII +68,00 € (Mietenstufen I–IV: keine Aufstockung).

### Saarland – Erhöhungsbeträge A 4–A 6

In Stufe 2 für das erste Kind in A 4–A 6: +17,91 €. Ab Stufe 3 für jedes weitere Kind: A 4 +71,65 €, A 5 +47,77 €, A 6 +23,88 €.

### Sachsen – Erhöhung A 5

In Stufe 2 für das erste Kind: +5,11 €. Ab Stufe 3 für jedes weitere Kind: +20,45 €.

### Sachsen-Anhalt – Erhöhung A 5

Für das erste Kind: +6,69 €. Für jedes weitere Kind: +20,11 €.

### Thüringen – veraltete Datenlage (Stand Februar 2025)

Keine 2026er-Tabelle beim dbb gefunden (bei praktisch allen anderen Ländern lag eine vor) – entweder hat Thüringen 2026 tatsächlich noch nicht angepasst, oder die Tabelle wurde beim dbb noch nicht veröffentlicht. **Vor Launch gezielt prüfen, ob es 2026 eine Anpassung gab.** Anrechnungsbetrag (separate Größe, kein Zuschlag): A 6–A 8: 148,94 €, A 9–A 12: 155,98 €.

## Bekannte Unsicherheiten / vor Launch zu klären

- **„Entwurf"-Status bei Baden-Württemberg, Bayern, Bremen**: dbb-Tabellen mit dem Vermerk "Veröffentlichung unter Vorbehalt der Bekanntmachung im Gesetzblatt" – vor Launch gegen die inzwischen verkündeten Gesetzblätter gegenprüfen.
- **Thüringen**: veraltete Datenlage (Februar 2025), keine 2026er-Anpassung gefunden – gezielt nachrecherchieren.
- **Berlin**: Ergänzender Familienzuschlag nach § 40a (Sonderfälle) ist komplex und im MVP-Rechner nicht abgebildet.
- **Baden-Württemberg**: einziges Land, bei dem die Erfahrungsstufe des Grundgehalts zusätzlich zur Besoldungsgruppe eine Rolle spielt (Familienergänzungszuschlag-Matrix) – für 100%ige Korrektheit bräuchte es ein zusätzliches Eingabefeld nur für dieses Land.
- Generell: Jährliche/unterjährige Anpassungen (Bund zum 01.05., die meisten Länder zum 01.04., einige zum 01.01.) bedeuten **laufenden Pflegeaufwand**. Ohne jährlichen Update-Prozess veraltet der Rechner schnell – siehe dazu bereits die Risiken-Sektion in [[02 Projekte/Fairbeamtet/Eigener Gehaltsrechner.md|Eigener Gehaltsrechner]].

**Empfehlung:** Die Datenqualität ist jetzt für 16 von 17 Dienstherren auf Primärquellen-Niveau (dbb-Besoldungstabellen, teils noch "Entwurf"-Status). Vor einem echten Go-Live: (1) Thüringen 2026 nachrecherchieren, (2) die drei "Entwurf"-Länder gegen die verkündeten Gesetzblätter prüfen, (3) mit Sven abstimmen, ob die komplexeren Sonderfälle (Berlin § 40a, Baden-Württemberg Erfahrungsstufe) im MVP ausgeklammert bleiben.

## Uniqueness-Check: Was macht unseren Rechner besser als die Konkurrenz?

Recherchiert 13.11.2026, zweite Runde (gezielt nach existierenden *interaktiven* Rechnern für Bayern/NRW gesucht, nicht nur statischen Tabellen – Korrektur gegenüber der ersten Einschätzung unten).

- **beamtenberater.com, oeffentlichen-dienst.de (Hauptartikel), tarifvertrag-online.de**: nur statische Tabellen/Fließtext zum Familienzuschlag selbst, kein interaktiver Rechner dafür. Teils unvollständig (nur Stufe 1 + 1. Kind, weitere Kinder "auf Einzelseiten").
- **einfachverbeamtet.de**: hat laut [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]] einen Familienzuschlag als Modul im großen Gehaltsrechner, aber nicht transparent in Methodik/Quellen.
- **Eigener fairbeamtet.de-Artikel**: nur Text + 2 Beispielrechnungen, kein eigenes Tool, genau wie beim BMI-Thema vor dem BMI-Rechner.

**Aber: Es gibt bereits mehrere Rechner, die Bayern und NRW trotz Ortsklassen-/Mietenstufen-Komplexität abdecken** – das ist kein unbesetztes Feld:
- **[Bezügerechner des BVA](https://bezuegerechner.bva.bund.de/rechner/beamte)**: offizieller Rechner des Bundesverwaltungsamts, aber nur für Bundesbeamte, nicht für Länder.
- **[oeffentlichen-dienst.de – Besoldungsrechner Bayern](https://www.oeffentlichen-dienst.de/beamte/besoldung/by/rechner.html)** und **[…NRW](https://www.oeffentlichen-dienst.de/beamte/besoldung/nrw/rechner.html)**: private Rechner mit Ortsklassen- bzw. Mietenstufen-Auswahl, berechnen die komplette Besoldung inkl. Familienzuschlag.
- **[besoldungsrechner.com/bayern](https://besoldungsrechner.com/bayern/)**: sehr detailliert – Besoldungsgruppe, Erfahrungsstufe, Ortsklasse (I–VII), Familienstand, "Partner im öffentlichen Dienst" (anteilige Regelung), Kinderzahl (0–8). Weist den Familienzuschlag in der Ergebnisübersicht **separat** aus ("Fam.Zuschlag Stufe V (Ehe)", "1. Kind", "2. Kind", "ab 3. Kind"). Kein Beratungs-CTA erkennbar, wirkt als reines Rechen-Tool ohne Lead-Mechanik.
- **[besoldungsrechner.com – NRW Mietenstufen-Überblick](https://besoldungsrechner.com/nrw-familienzuschlag-mietenstufe-unterschiede)**: eigene Tabellenseite nur zu diesem Thema, verweist auf den vollen Rechner.
- **[BBB-Rechner „Orts- und Familienzuschlag"](https://www.bbb-bayern.de/service/bbb-rechner-orts-und-familienzuschlag/)**: Rechner des Bayerischen Beamtenbunds, aber **nur für BBB-Mitglieder** zugänglich (App/Mitgliederportal), kein frei zugängliches Web-Tool. Nach eigener Aussage keine Günstigerprüfung und keine Nachzahlungsprüfung.
- **[tarifvertrag-online.de/familienzuschlag/nrw](https://tarifvertrag-online.de/familienzuschlag/nrw)** und **[…/bayern](https://tarifvertrag-online.de/familienzuschlag/bayern)**: statische Tabellen nach Mietenstufe/Ortsklasse, kein Rechner, aber immerhin vollständiger als die Hauptübersichtsseite.

**Einordnung:** Ein frei zugänglicher, werbefreier Rechner *speziell* für den Familienzuschlag (statt als Nebenprodukt eines kompletten Besoldungsrechners) existiert nicht. Die eigentliche Lücke ist also nicht "gibt es sowas schon", sondern: **kein Wettbewerber verbindet das mit Transparenz zu Datenqualität/Gültigkeit und einer ehrlichen Beratungs-CTA statt reiner Zahlenausgabe.** Unser Rechner sollte sich entsprechend positionieren – fokussiert auf den Familienzuschlag allein (schneller, einfacher als ein kompletter Besoldungsrechner mit 10+ Feldern), mit sichtbarem Gültigkeitsdatum/Vertrauens-Hinweis je Bundesland, und dort, wo die Datenlage nicht sauber ist (aktuell Bayern/NRW/Thüringen), ehrlich blockierend statt einen falschen Pseudo-Wert auszugeben.

## Rechner-Konzept (Version 2 – vollständig, nach Besoldungsgruppe)

Grundüberarbeitung gegenüber Version 1: Ines wollte einen Rechner, der **für jedes Bundesland, jede Besoldungsgruppe und jede Familienkonstellation** funktioniert, nicht nur den Standardfall. Dafür war ein neues Eingabefeld (Besoldungsgruppe) nötig, plus zwei konditionale Felder für die zwei Länder mit echter Ortsabhängigkeit.

**Eingaben:**
- Bundesland (Dropdown, 17 Optionen: Bund + 16 Länder)
- **Besoldungsgruppe (neu)**: Dropdown A 3–A 16 plus "B-Besoldung / höherer Dienst" als Sammelkategorie. Steuert alle besoldungsgruppenabhängigen Erhöhungsbeträge (siehe Recherche-Abschnitt oben).
- Verheiratet/verpartnert (Ja/Nein)
- Anzahl kindergeldberechtigter Kinder (Zahl, 0–8)
- **Ortsklasse (neu, nur bei Bayern sichtbar)**: Dropdown I–VII
- **Mietenstufe (neu, nur bei NRW und Rheinland-Pfalz sichtbar)**: Dropdown I–VII (bei NRW zwingend für die Berechnung, bei Rheinland-Pfalz nur für den Kind-3+-Aufschlag relevant)

**Rechenlogik, drei Typen:**
1. **Additiv** (14 von 17 Dienstherren): Ehe-/Partnerschaftsanteil (ggf. nach Besoldungsgruppenband) + ein Kinderanteil-Satz für Kind 1, Kind 2, Kind 3 und Kind 4+ (bei den meisten Ländern sind Kind 1 und Kind 2 gleich, Kind 3+ ist der große Sprung). Besoldungsgruppen-Erhöhungsbeträge werden als Zuschlag auf den jeweiligen Kind-Satz aufgeschlagen.
2. **Bayern**: Ortsklasse bestimmt Stufe V/1/2/zzgl.3.Kind/zzgl.weiteres – daraus werden die gleichen vier Kind-Sätze abgeleitet wie beim additiven Modell, zusätzlich eine Besoldungsgruppen-Erhöhung (A 3–A 10) je Kind und Ortsklasse.
3. **NRW**: echte dreidimensionale Lookup-Tabelle (Besoldungsgruppenband × Mietenstufe × Kinderzahl), keine Addition – siehe Begründung oben.

**Ausgabe:**
- Monatlicher Familienzuschlag, aufgeschlüsselt nach Ehe-/Partnerschaftsanteil, Kinderanteil (inkl. eingerechneter Besoldungsgruppen-Zuschläge) und Gesamtsumme
- Gültigkeitsdatum und Status-Badge (final verkündet / Entwurf / veraltet – siehe Thüringen)
- Separate Ausweisung von Zusatzleistungen, die **nicht** in der Summe enthalten sind (Bremen: Familienergänzungszuschlag; Baden-Württemberg: Erfahrungsstufen-abhängiger Familienergänzungszuschlag; Berlin: Ergänzender Familienzuschlag nach § 40a) – als eigene Zeile mit Hinweis, nicht stillschweigend weggelassen
- CTA zur Beratung bleibt erhalten, auch wenn jetzt (fast) immer eine Zahl ausgegeben wird

## Layout

Gleiche Markenbasis wie [[02 Projekte/Fairbeamtet/BMI-Rechner.md|BMI-Rechner]], damit beide Tools als zusammengehörige „Rechner-Familie" wirken: Anton für Headlines/große Zahlen, Inter für Fließtext, Navy `#0B1E33` als Hero-/Ergebnis-Hintergrund, Pink/Magenta `#FF3F77` als Akzent- und CTA-Farbe, Blau `#0693E3` für Formularelemente. Gleiches Karten-/Stat-Kachel-Muster, gleiche Kontaktkarte am Ende (Platzhalter-Kreise statt Fotos, wie beim BMI-Rechner).

## Code

Entwurf, fachlich **noch nicht freigegeben**. Die Datenbasis (`FZ_DATEN`) ist absichtlich so gebaut, dass Bundesländer mit `stufe1: null` oder `kind: null` keine Berechnung ausgeben, sondern einen Hinweis – das verhindert, dass unsichere Zahlen als Ergebnis ausgespielt werden, bevor der Primärquellen-Check gemacht ist.

```html
<div class="fb-fz-rechner">
  <div class="fb-fz-hero">
    <div class="fb-fz-hero-watermark" aria-hidden="true">€</div>
    <div class="fb-fz-hero-inner">
      <p class="fb-fz-eyebrow">FAMILIENZUSCHLAG 2026</p>
      <h1>DEIN ZUSCHLAG.<br><span class="fb-fz-accent">DEIN BUNDESLAND.</span></h1>
      <p class="fb-fz-intro">Verheiratet, verpartnert, mit Kindern? Der Familienzuschlag unterscheidet sich je Bundesland teils deutlich. Trag deine Situation ein, ich zeig dir deinen monatlichen Zuschlag.</p>
      <a href="#fbFzForm" class="fb-fz-hero-button">Jetzt berechnen <span aria-hidden="true">&rarr;</span></a>
    </div>
  </div>

  <div class="fb-fz-stat-row">
    <div class="fb-fz-stat-tile">
      <div class="fb-fz-stat-number">17</div>
      <p>Dienstherren (Bund + 16 Länder) mit jeweils eigener Besoldungsregel seit der Föderalismusreform 2006.</p>
    </div>
    <div class="fb-fz-stat-tile fb-fz-stat-tile-accent">
      <div class="fb-fz-stat-number">AB KIND 3</div>
      <p>In fast allen Bundesländern springt der Kinderanteil ab dem dritten Kind deutlich nach oben.</p>
    </div>
    <div class="fb-fz-stat-tile">
      <div class="fb-fz-stat-number">JÄHRLICH</div>
      <p>Die Beträge werden regelmäßig angepasst – meist zum 1. April, beim Bund zum 1. Mai.</p>
    </div>
  </div>

  <div class="fb-fz-grid">
    <div class="fb-fz-form-card" id="fbFzForm-anchor">
      <form id="fbFzForm">
        <div class="fb-fz-fields">
          <label class="fb-fz-field">
            Bundesland / Dienstherr
            <select id="fbFzLand" required>
              <option value="bund">Bund</option>
              <option value="bw">Baden-Württemberg</option>
              <option value="by">Bayern</option>
              <option value="be">Berlin</option>
              <option value="bb">Brandenburg</option>
              <option value="hb">Bremen</option>
              <option value="hh">Hamburg</option>
              <option value="he">Hessen</option>
              <option value="mv">Mecklenburg-Vorpommern</option>
              <option value="ni">Niedersachsen</option>
              <option value="nw">Nordrhein-Westfalen</option>
              <option value="rp">Rheinland-Pfalz</option>
              <option value="sl">Saarland</option>
              <option value="sn">Sachsen</option>
              <option value="st">Sachsen-Anhalt</option>
              <option value="sh">Schleswig-Holstein</option>
              <option value="th">Thüringen</option>
            </select>
          </label>

          <label class="fb-fz-field fb-fz-field-checkbox">
            <input type="checkbox" id="fbFzVerheiratet">
            Verheiratet / verpartnert
          </label>

          <label class="fb-fz-field">
            Anzahl kindergeldberechtigter Kinder
            <input type="number" id="fbFzKinder" min="0" max="10" step="1" value="0" required>
          </label>
        </div>

        <button type="submit" class="fb-fz-button">Berechnen</button>
      </form>
    </div>

    <div class="fb-fz-result-card">
      <div class="fb-fz-placeholder" id="fbFzPlaceholder">
        <p>Wähl links dein Bundesland und deine Familiensituation. Ich zeig dir deinen monatlichen Familienzuschlag.</p>
      </div>

      <div class="fb-fz-result" id="fbFzResult" hidden>
        <div class="fb-fz-number"><span id="fbFzValue">0</span><span class="fb-fz-unit">€/Monat</span></div>
        <div class="fb-fz-breakdown" id="fbFzBreakdown"></div>
        <p class="fb-fz-kommentar" id="fbFzKommentar"></p>
      </div>

      <div class="fb-fz-unklar" id="fbFzUnklar" hidden>
        <p id="fbFzUnklarText"></p>
        <a href="#" class="fb-fz-cta-button-inline">Meinen Zuschlag konkret klären lassen <span aria-hidden="true">&rarr;</span></a>
      </div>
    </div>
  </div>

  <div class="fb-fz-infobox">
    <h2>So funktioniert der Familienzuschlag</h2>
    <p>Der Familienzuschlag ergänzt deine Besoldung je nach Familienstand. Verheiratete oder verpartnerte Beamtinnen und Beamte erhalten die sogenannte Stufe 1. Für jedes kindergeldberechtigte Kind kommt zusätzlich ein kinderbezogener Anteil hinzu, der ab dem dritten Kind in fast allen Bundesländern deutlich höher ausfällt.</p>
    <p>Seit der Föderalismusreform 2006 legt jedes Bundesland seinen Familienzuschlag selbst im eigenen Landesbesoldungsgesetz fest – deshalb unterscheiden sich die Beträge teils erheblich, und manche Länder (z. B. Berlin, Brandenburg) zahlen gar keinen klassischen Ehe-/Partnerschaftsanteil mehr.</p>
    <p>Wichtig: Dieser Rechner bildet den <strong>klassischen</strong> Familienzuschlag ab. Mehrere Länder zahlen zusätzlich einen Familienergänzungszuschlag nach Besoldungsgruppe, der hier nicht eingerechnet ist. Bei Bayern und Nordrhein-Westfalen hängt der Betrag zusätzlich von Ortsklasse bzw. Mietenstufe ab – dafür geben wir hier bewusst keinen Pauschalwert aus. Mehr Hintergrund in unserem <a href="https://www.fairbeamtet.de/familienzuschlag-fuer-beamte/">ausführlichen Artikel zum Familienzuschlag</a>.</p>
  </div>

  <div class="fb-fz-contact-card">
    <div class="fb-fz-contact-photos" aria-hidden="true">
      <div class="fb-fz-contact-photo"></div>
      <div class="fb-fz-contact-photo"></div>
      <div class="fb-fz-contact-photo"></div>
    </div>
    <div class="fb-fz-contact-text">
      <p class="fb-fz-contact-label">DEINE ANSPRECHPARTNER</p>
      <h2>Fragen zu deiner Besoldung?</h2>
      <p>Der Familienzuschlag ist nur ein Baustein deiner Besoldung. Willst du wissen, was er für deine Vorsorge oder Absicherung bedeutet? Dann lass uns das gemeinsam klären, unverbindlich und kostenlos.</p>
      <a href="#" class="fb-fz-cta-button">Kostenloses Gespräch vereinbaren <span aria-hidden="true">&rarr;</span></a>
    </div>
  </div>
</div>

<style>
@import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');
/* Entwurfs-Hinweis: direkter Google-Fonts-Import ist nur fuer den Vorschlags-Entwurf okay.
   Vor Go-Live selbst hosten, siehe Layout-Entscheidungen im BMI-Rechner. */

.fb-fz-rechner {
  max-width: 1100px;
  margin: 0 auto;
  padding: 48px 24px;
  font-family: 'Inter', sans-serif;
  color: #1A1A1A;
}
.fb-fz-rechner h1,
.fb-fz-rechner h2,
.fb-fz-stat-number,
.fb-fz-number {
  font-family: 'Anton', 'Inter', sans-serif;
  font-weight: 400;
  text-transform: uppercase;
  letter-spacing: 0.01em;
}

.fb-fz-hero {
  position: relative;
  background: #0B1E33;
  color: #fff;
  border-radius: 20px;
  padding: 64px 40px;
  margin-bottom: 24px;
  text-align: center;
  overflow: hidden;
}
.fb-fz-hero-watermark {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-family: 'Anton', sans-serif;
  font-size: clamp(8rem, 28vw, 18rem);
  color: rgba(255,255,255,0.1) !important;
  white-space: nowrap;
  pointer-events: none;
  line-height: 1;
}
.fb-fz-hero-inner {
  position: relative;
  z-index: 1;
}
.fb-fz-eyebrow {
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  color: #7FC4F0 !important;
  margin: 0 0 16px 0;
}
.fb-fz-hero h1 {
  font-size: clamp(2.4rem, 6vw, 4.2rem);
  margin: 0 0 20px 0;
  line-height: 1.02;
  color: #fff !important;
}
.fb-fz-accent {
  color: #FF3F77 !important;
}
.fb-fz-hero .fb-fz-intro {
  max-width: 640px;
  margin: 0 auto;
  font-size: 1.1rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.9) !important;
}
.fb-fz-hero-button {
  display: inline-block;
  margin-top: 28px;
  background: #FF3F77;
  color: #fff;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 30px;
  font-family: 'Inter', sans-serif;
  font-weight: 700;
}
.fb-fz-hero-button:hover {
  background: #D92F5F;
}

.fb-fz-stat-row {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-bottom: 32px;
}
@media (max-width: 760px) {
  .fb-fz-stat-row {
    grid-template-columns: 1fr;
  }
}
.fb-fz-stat-tile {
  background: #F4F6FA;
  border-radius: 14px;
  padding: 24px;
}
.fb-fz-stat-tile-accent {
  background: #FF3F77;
  color: #fff;
}
.fb-fz-stat-tile-accent p {
  color: rgba(255,255,255,0.92);
}
.fb-fz-stat-number {
  font-size: 2rem;
  line-height: 1;
  margin-bottom: 8px;
}
.fb-fz-stat-tile p {
  margin: 0;
  font-size: 0.92rem;
  line-height: 1.5;
}

.fb-fz-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
  align-items: start;
  margin-bottom: 32px;
}

.fb-fz-form-card,
.fb-fz-result-card {
  border-radius: 16px;
  padding: 32px;
}
.fb-fz-form-card {
  background: #fff;
  border: 1px solid #E2E6EE;
  box-shadow: 0 10px 30px rgba(15,30,51,0.06);
}
.fb-fz-result-card {
  background: #0B1E33;
  color: #fff !important;
  min-height: 220px;
  padding: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.fb-fz-result-card * {
  color: inherit;
}

.fb-fz-fields {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-bottom: 20px;
}
@media (max-width: 560px) {
  .fb-fz-fields {
    grid-template-columns: 1fr;
  }
}
.fb-fz-field {
  display: flex;
  flex-direction: column;
  gap: 6px;
  font-weight: 600;
  font-size: 0.95rem;
}
.fb-fz-field-checkbox {
  flex-direction: row;
  align-items: center;
  gap: 10px;
}
.fb-fz-field select,
.fb-fz-field input[type="number"] {
  background: #fff !important;
  color: #1A1A1A !important;
  font-family: 'Inter', sans-serif;
  font-size: 1.05rem;
  padding: 14px 16px;
  border: 1px solid #D6DCE8;
  border-radius: 10px;
  box-sizing: border-box;
  width: 100%;
}
.fb-fz-field select:focus,
.fb-fz-field input:focus {
  outline: none;
  border-color: #0693E3;
}
.fb-fz-field input[type="checkbox"] {
  width: 20px;
  height: 20px;
  accent-color: #0693E3;
}

.fb-fz-button {
  font-family: 'Inter', sans-serif;
  background: #0693E3;
  color: #fff;
  border: none;
  border-radius: 999px;
  padding: 16px 28px;
  font-size: 1.05rem;
  font-weight: 700;
  cursor: pointer;
  width: 100%;
}
.fb-fz-button:hover {
  background: #057AB0;
}

.fb-fz-placeholder {
  text-align: center;
  font-size: 1.02rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.8) !important;
}
.fb-fz-placeholder p {
  color: inherit !important;
}
.fb-fz-result {
  text-align: center;
  width: 100%;
}
.fb-fz-number {
  font-size: 4.2rem;
  line-height: 1;
  color: #fff !important;
}
.fb-fz-unit {
  font-size: 1.4rem;
  margin-left: 8px;
  color: #FF6FB5 !important;
}
.fb-fz-breakdown {
  margin: 18px 0;
  font-family: 'Inter', sans-serif;
  text-transform: none;
  font-size: 0.95rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.85) !important;
}
.fb-fz-kommentar {
  font-size: 0.9rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.7) !important;
}
.fb-fz-unklar {
  text-align: center;
  width: 100%;
}
.fb-fz-unklar p {
  font-size: 1rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.9) !important;
  margin-bottom: 20px;
}
.fb-fz-cta-button-inline {
  display: inline-block;
  background: #FF3F77;
  color: #fff !important;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 28px;
  font-weight: 700;
  font-family: 'Inter', sans-serif;
}
.fb-fz-cta-button-inline:hover {
  background: #D92F5F;
}

.fb-fz-infobox {
  background: #F4F6FA;
  padding: 32px;
  border-radius: 16px;
  line-height: 1.6;
}
.fb-fz-infobox h2 {
  margin-top: 0;
  font-size: 1.7rem;
}

.fb-fz-contact-card {
  display: flex;
  gap: 24px;
  align-items: flex-start;
  background: #F4F6FA;
  border-radius: 16px;
  padding: 32px;
  margin-top: 24px;
}
@media (max-width: 560px) {
  .fb-fz-contact-card {
    flex-direction: column;
  }
}
.fb-fz-contact-photos {
  flex: 0 0 auto;
  display: flex;
}
.fb-fz-contact-photo {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  background: #0693E3;
  border: 3px solid #F4F6FA;
  margin-left: -16px;
}
.fb-fz-contact-photo:first-child {
  margin-left: 0;
  background: #9F4CFF;
}
.fb-fz-contact-photo:last-child {
  background: #FF3F77;
}
.fb-fz-contact-label {
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  color: #0693E3;
  margin: 0 0 4px 0;
}
.fb-fz-contact-text h2 {
  margin: 0 0 12px 0;
  font-size: 1.5rem;
  text-transform: none;
}
.fb-fz-contact-text p {
  margin: 0 0 16px 0;
  line-height: 1.6;
}
.fb-fz-cta-button {
  display: inline-block;
  background: #FF3F77;
  color: #fff;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 28px;
  font-weight: 700;
  font-family: 'Inter', sans-serif;
}
.fb-fz-cta-button:hover {
  background: #D92F5F;
}
</style>

<script>
(function() {
  // Stand der Recherche: 13.11.2026, Sekundärquellen – siehe Projektnotiz "Familienzuschlag-Rechner".
  // stufe1/kind/ab3 = null bedeutet: keine verlässliche Pauschalzahl verfügbar (Ortsklassen/Mietenstufen
  // oder widersprüchliche Quellen). In diesen Fällen wird bewusst NICHT gerechnet.
  var FZ_DATEN = {
    bund: { name: 'Bund', stufe1: 181.36, kind: 154.99, ab3: 482.89, gueltig: '01.05.2026', verlaesslich: true, hinweis: null },
    bw:   { name: 'Baden-Württemberg', stufe1: 180.46, kind: 157.78, ab3: 989.17, gueltig: '01.04.2026', verlaesslich: true, hinweis: 'Zusätzlicher Familienergänzungszuschlag nach Besoldungsgruppe (A 7–A 10) ist hier nicht eingerechnet.' },
    by:   { name: 'Bayern', stufe1: null, kind: null, ab3: null, gueltig: '01.10.2026', verlaesslich: false, hinweis: 'Bayern staffelt den Familienzuschlag nach 7 Ortsklassen – ein pauschaler Betrag wäre hier irreführend.' },
    be:   { name: 'Berlin', stufe1: 0, kind: 148.44, ab3: 819.76, gueltig: '01.04.2026', verlaesslich: true, hinweis: 'Berlin zahlt keinen klassischen Ehe-/Partnerschaftsanteil mehr (ggf. Ausgleichszulage für Altfälle, hier nicht eingerechnet).' },
    bb:   { name: 'Brandenburg', stufe1: 0, kind: 377.16, ab3: 888.39, gueltig: '01.07.2024', verlaesslich: false, hinweis: 'Brandenburg zahlt keinen ehebezogenen Anteil. Datenstand älter als bei den anderen Ländern – vor Verwendung prüfen.' },
    hb:   { name: 'Bremen', stufe1: 161.00, kind: 258.89, ab3: 610.60, gueltig: '01.04.2026', verlaesslich: false, hinweis: 'Richtwert – Bremen staffelt zusätzlich nach Besoldungsgruppe (A 5–A 8), der genaue Betrag kann abweichen.' },
    hh:   { name: 'Hamburg', stufe1: 165.84, kind: 193.14, ab3: 635.00, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    he:   { name: 'Hessen', stufe1: 177.30, kind: 360.57, ab3: 831.08, gueltig: '01.07.2026', verlaesslich: true, hinweis: null },
    mv:   { name: 'Mecklenburg-Vorpommern', stufe1: 164.77, kind: 198.83, ab3: 820.00, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    ni:   { name: 'Niedersachsen', stufe1: 162.26, kind: 145.61, ab3: 512.37, gueltig: '01.04.2026', verlaesslich: true, hinweis: 'Wert für Besoldungsgruppen A 5–A 8, in höheren Gruppen bis 170,36 € Stufe 1.' },
    nw:   { name: 'Nordrhein-Westfalen', stufe1: null, kind: null, ab3: null, gueltig: '01.04.2026', verlaesslich: false, hinweis: 'NRW staffelt zusätzlich nach Mietenstufe (I–VII) und Besoldungsgruppe – ein pauschaler Betrag wäre hier irreführend.' },
    rp:   { name: 'Rheinland-Pfalz', stufe1: 88.03, kind: 246.97, ab3: 726.00, gueltig: '01.04.2026', verlaesslich: false, hinweis: 'Der Stufe-1-Betrag wirkt im Ländervergleich ungewöhnlich niedrig – vor Veröffentlichung gegen das Landesbesoldungsgesetz prüfen.' },
    sl:   { name: 'Saarland', stufe1: 164.48, kind: 165.31, ab3: 781.68, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    sn:   { name: 'Sachsen', stufe1: 279.58, kind: 279.58, ab3: 795.41, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    st:   { name: 'Sachsen-Anhalt', stufe1: 169.04, kind: 184.85, ab3: 818.98, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    sh:   { name: 'Schleswig-Holstein', stufe1: 176.24, kind: 199.85, ab3: 516.48, gueltig: '01.01.2026', verlaesslich: true, hinweis: null },
    th:   { name: 'Thüringen', stufe1: null, kind: null, ab3: null, gueltig: '01.04.2026', verlaesslich: false, hinweis: 'Die Kinderanteile sind in den verfügbaren Quellen widersprüchlich – vor Veröffentlichung gegen das Thüringer Besoldungsgesetz prüfen.' }
  };

  var form = document.getElementById('fbFzForm');
  var placeholder = document.getElementById('fbFzPlaceholder');
  var result = document.getElementById('fbFzResult');
  var unklar = document.getElementById('fbFzUnklar');
  var unklarText = document.getElementById('fbFzUnklarText');
  var valueEl = document.getElementById('fbFzValue');
  var breakdownEl = document.getElementById('fbFzBreakdown');
  var kommentarEl = document.getElementById('fbFzKommentar');

  function formatEuro(betrag) {
    return betrag.toLocaleString('de-DE', { minimumFractionDigits: 2, maximumFractionDigits: 2 });
  }

  form.addEventListener('submit', function(e) {
    e.preventDefault();

    var landKey = document.getElementById('fbFzLand').value;
    var verheiratet = document.getElementById('fbFzVerheiratet').checked;
    var kinder = parseInt(document.getElementById('fbFzKinder').value, 10) || 0;
    var daten = FZ_DATEN[landKey];

    if (daten.stufe1 === null || daten.kind === null) {
      placeholder.hidden = true;
      result.hidden = true;
      unklar.hidden = false;
      unklarText.textContent = 'Für ' + daten.name + ' lässt sich der Familienzuschlag nicht seriös pauschal berechnen: ' + daten.hinweis;
      return;
    }

    var eheAnteil = verheiratet ? daten.stufe1 : 0;
    var kinderAnteil = 0;
    for (var i = 1; i <= kinder; i++) {
      kinderAnteil += (i <= 2) ? daten.kind : daten.ab3;
    }
    var summe = eheAnteil + kinderAnteil;

    var zeilen = [];
    if (verheiratet) {
      zeilen.push('Ehe-/Partnerschaftsanteil (Stufe 1): ' + formatEuro(eheAnteil) + ' €');
    }
    if (kinder > 0) {
      zeilen.push('Kinderanteil für ' + kinder + ' Kind' + (kinder === 1 ? '' : 'er') + ': ' + formatEuro(kinderAnteil) + ' €');
    }
    if (zeilen.length === 0) {
      zeilen.push('Ohne Ehe-/Partnerschaft und ohne Kinder entsteht kein Familienzuschlag.');
    }

    valueEl.textContent = formatEuro(summe);
    breakdownEl.innerHTML = zeilen.map(function(z) { return '<div>' + z + '</div>'; }).join('');

    var kommentar = daten.name + ', gültig ab ' + daten.gueltig + '.';
    if (!daten.verlaesslich) {
      kommentar += ' Hinweis: ' + daten.hinweis;
    } else if (daten.hinweis) {
      kommentar += ' ' + daten.hinweis;
    }
    kommentarEl.textContent = kommentar;

    placeholder.hidden = true;
    unklar.hidden = true;
    result.hidden = false;
  });
})();
</script>
```

## Hinweise zur Einbindung

- Gleiche Schrift-/Farb-Basis wie [[02 Projekte/Fairbeamtet/BMI-Rechner.md|BMI-Rechner]] – siehe dort zu DSGVO-Pflicht beim Self-Hosting der Schrift vor Go-Live.
- Kontaktkarte mit Foto-Platzhaltern, analog zum BMI-Rechner – echte Fotos aus [[00 Kontext/Fairbeamtet/Team.md|Team]] einsetzen, sobald verfügbar.
- CTA-Links sind Platzhalter (`#`) – echte URL zur Beratungs-/Kontaktseite einsetzen.
- Die Datenstruktur `FZ_DATEN` ist bewusst so gebaut, dass sie sich künftig leicht aktualisieren lässt (ein Objekt pro Bundesland) – das deckt sich mit der in [[02 Projekte/Fairbeamtet/Eigener Gehaltsrechner.md|Eigener Gehaltsrechner]] geforderten zentralen Datenpflege statt händischer Einzelpflege pro Seite.

## Nächste Schritte

- [ ] Primärquellen-Check gegen die jeweiligen Landesbesoldungsgesetze – mindestens für die als „niedrig" markierten Länder (Bayern, NRW, Thüringen, Rheinland-Pfalz, Bremen, Brandenburg)
- [ ] Entscheiden, wie mit Bayern/NRW umgegangen wird: volle Ortsklassen-/Mietenstufen-Matrix einpflegen oder bewusst nur mit Hinweistext + CTA arbeiten (aktueller Stand im Code)
- [ ] Mit Sven abstimmen: fachliche Freigabe der Zahlen, Platzierung auf der Seite (eigenständige Rechner-Seite vs. Einbindung im bestehenden Artikel)
- [ ] Echten Link zur Beratungs-/Kontaktseite einsetzen
- [ ] Jährlichen Update-Prozess für die Zahlen festlegen (mehrere Länder passen zum 1. April an, der Bund zum 1. Mai)
- [ ] Erst nach Freigabe: live schalten
