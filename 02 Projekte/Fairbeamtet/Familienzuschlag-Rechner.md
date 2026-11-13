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

**Entwurf – inzwischen von Sven teilweise faktengeprüft (13.11.2026), noch nicht vollständig abgestimmt.** Die Datenlage hat sich gegenüber der ersten Version grundlegend verbessert: Fast alle Zahlen sind jetzt gegen **offizielle Besoldungstabellen des dbb (Deutscher Beamtenbund und Tarifunion)** geprüft, nicht mehr gegen Sekundärquellen-Aggregatoren. Sven hat zusätzlich die Bund-Werte unabhängig gegen die Anlage V BBesG nachgerechnet und bestätigt (siehe Bund-Detailabschnitt unten) – die Zahlen stimmten bereits, der Status war falsch deklariert. Drei Einschränkungen bleiben:
1. Mehrere dbb-Tabellen (Baden-Württemberg, Bayern, Bremen, u. a.) tragen den Vermerk **„Entwurf – Veröffentlichung unter Vorbehalt der Bekanntmachung im Gesetzblatt"** – die Zahlen stammen aus dem Gesetzgebungsverfahren, sind aber zum Abrufzeitpunkt (13.11.2026) noch nicht formal im jeweiligen Gesetzblatt verkündet. Hohe Wahrscheinlichkeit, dass sie final so gelten, aber kein Ersatz für eine Gesetzblatt-Prüfung vor Launch.
2. **Bund ist kein "Entwurf", sondern ein vorläufiger Abschlag ohne Gesetzesgrundlage** (eigener Status "abschlag") – das Bundesalimentationsgesetz dazu hat noch keinen Kabinettsbeschluss, ein früherer Entwurf hätte sogar den Ehe-/Partnerschaftsanteil gestrichen. Diese Unterscheidung war vorher nicht abgebildet.
3. Thüringen: keine dbb-Tabelle für 2026 gefunden, nur Stand 1. Februar 2025.

**Vor Veröffentlichung weiterhin empfohlen:** kurzer Abgleich der "Entwurf"-Länder gegen die zwischenzeitlich verkündeten Gesetzblätter, analog zur Vorgabe beim BMI-Rechner (Rangfolge Voice Profile Punkt 1: fachliche Richtigkeit schlägt alles andere).

## Rechtliche Grundlage

Bundesbeamte: § 40 BBesG. Landesbeamte: seit der Föderalismusreform 2006 die jeweiligen 16 Landesbesoldungsgesetze (eigene Anlagen zum Familienzuschlag, nicht mehr bundeseinheitlich). Das ist auch der Grund, warum die Struktur zwischen den Ländern so stark variiert (manche ganz ohne „Stufe 1", manche mit Besoldungsgruppen- oder Ortsklassen-/Mietenstufen-Abhängigkeit).

## Recherche: Familienzuschlag nach Bundesland – vollständige Daten (Primärquelle: dbb-Besoldungstabellen, Stand der Recherche: 13.11.2026)

Komplett neu recherchiert über die offiziellen Besoldungstabellen des dbb ([dbb.de/beamtinnen-beamte/besoldungstabellen.html](https://www.dbb.de/beamtinnen-beamte/besoldungstabellen.html)), jeweils die aktuellste 2026er-Fassung pro Bundesland heruntergeladen und direkt aus dem PDF ausgelesen (nicht per automatisiertem Seitenabruf mit kleinem Hilfsmodell, sondern mit Skript-Extraktion des PDF-Texts – das vermeidet die Rowspan-/OCR-Fehler, die bei der ersten Bayern/NRW-Recherche aufgetreten waren).

**Grundwerte (Standardfall: übrige/häufigste Besoldungsgruppe, keine Orts-/Mietenstufe):**

| Bundesland | Stufe 1 (verheiratet/verpartnert) | 1. Kind | 2. Kind | ab 3. Kind | Gültig ab | Quellenstatus |
|---|---|---|---|---|---|---|
| Bund | 181,36 € | +154,99 € (Stufe 2 gesamt: 336,35 €) | +154,99 € | +482,89 € je Kind | 01.05.2026 | **vorläufiger Abschlag, kein Gesetz** (Faktencheck Sven 13.11.2026, s. u.) |
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

### Bund – Faktencheck durch Sven (13.11.2026): Zahlen stimmen, Status war falsch

Sven hat die Bund-Werte unabhängig gegengerechnet und bestätigt: **974,23 € für verheiratet + 3 Kinder stimmt.** Herleitung, ausgehend von der tatsächlich geltenden **Anlage V BBesG (Stand 01.03.2024)**, zzgl. zweier Erhöhungsschritte (+3,0 % ab 01.04.2025, +2,8 % ab 01.05.2026, nach jedem Schritt gerundet):

| Bestandteil | Anlage V (03/2024) | × 1,03 | × 1,028 |
|---|---|---|---|
| Stufe 1 (verheiratet) | 171,28 € | 176,42 € | **181,36 €** |
| 1. Kind | 146,38 € | 150,77 € | **154,99 €** |
| 2. Kind | 146,38 € | 150,77 € | **154,99 €** |
| 3. Kind | 456,06 € | 469,74 € | **482,89 €** |

Drei unabhängige Quellen (Sven, tarifvertrag-online.de, oeffentlichen-dienst.de) kommen auf exakt dieselben Cent-Beträge – die **Zahlen im Rechner waren also schon richtig**. Was nicht gestimmt hat, war die Einordnung als "final verkündet":

1. **Die Mai-2026-Erhöhung ist ein vorläufiger Abschlag, kein verkündetes Gesetz.** Grundlage wäre das Bundesalimentationsgesetz – dafür gab es laut dbb zum 27.10.2026 weder einen Kabinettsbeschluss noch einen abgestimmten Entwurf. Bundesinnenminister Dobrindt kündigte am 02.11.2026 an, das Gesetz noch 2026 ins Kabinett zu bringen. **Status im Rechner jetzt auf "Vorläufiger Abschlag, kein Gesetz" geändert** (statt "final verkündet").
2. **Ein früherer Referentenentwurf (April 2026) hätte den Ehe-/Partnerschaftsanteil ab 2026 komplett gestrichen** – nur noch Kinderanteile (265 € für 1./2. Kind, 708 € für 3. Kind, laut oeffentlicher-dienst.org). Das BMI hat diesen Entwurf zurückgezogen und überarbeitet ihn; wie der Familienzuschlag am Ende aussieht, ist offen. Entsprechender Hinweistext jetzt im Ergebnis hinterlegt.
3. **Ortsklasse/Mietenstufe spielen beim Bund keine Rolle** – das war schon in der Rechenlogik korrekt (Bund nutzt weder Ortsklasse- noch Mietenstufen-Daten), aber die beiden Felder waren auf der Live-Seite trotzdem sichtbar, obwohl Bund ausgewählt war (Anzeige-Bug, nicht Rechenfehler – behoben, siehe "Bekannte Unsicherheiten"). Außerdem war die Formulierung "(inkl. Besoldungsgruppen-/Mietenstufen-Zuschlag)" in der Kinderanteil-Zeile bei A 9 irreführend, weil bei A 9 gar kein Zuschlag greift (nur A 3–A 5 haben beim Bund einen) – die Zeile nennt den Zusatz jetzt nur noch, wenn er tatsächlich eingerechnet wurde.
4. **Zwei Fälle fehlten komplett:** Ist der Ehepartner/die Ehepartnerin ebenfalls im öffentlichen Dienst, gibt es Stufe 1 nur anteilig (§ 40 BBesG). Den Kinderanteil bekommt nur, wer das Kindergeld bezieht. Beides jetzt als Hinweis im Rechner ergänzt (Infobox + Disclaimer unter dem Ergebnis) – nicht als Berechnung, weil das ein eigenes Eingabefeld bräuchte und für ein MVP zu weit ginge.

**Einschränkung von Sven selbst:** Er hat nur die Anlage V aus dem Gesetzestext nachgerechnet, nicht den amtlichen Abschlagsbescheid vom BVA bzw. der jeweiligen Bezügestelle – dass dort identisch gerundet wird, ist nicht belegt, aber angesichts von drei übereinstimmenden unabhängigen Quellen sehr wahrscheinlich.

Quellen (Sven, abgerufen 13.11.2026):
- [Anlage V BBesG, gesetze-im-internet.de](https://www.gesetze-im-internet.de/bbesg/anlage_v.html)
- [tarifvertrag-online.de – Familienzuschlag Bund](https://tarifvertrag-online.de/familienzuschlag/bund)
- [oeffentlichen-dienst.de – Familienzuschlag 2026](https://www.oeffentlichen-dienst.de/beamte/besoldung/familienzuschlag.html)
- [oeffentlicher-dienst.org – Referentenentwurf Bundesalimentationsgesetz](https://oeffentlicher-dienst.org/beamte/bund/bundesalimentationsgesetz)
- [oeffentlicher-dienst-news.de – Dobrindts Zeitplan](https://oeffentlicher-dienst-news.de/dobrindt-will-besoldungsgesetz-fuer-bundesbeamte-noch-2026-beschliessen/)
- [beamten-starter.de – Stand Alimentation Bund](https://www.beamten-starter.de/amtsangemessene-alimentation-bund.html)
- [verdi.de – Neuer Zeitplan](https://www.verdi.de/ikt/themen/beamtenpolitik/neuer-zeitplan-fuer-verfassungskonforme-besoldung)

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
- **Durchgängiger "Ohne Gewähr"-Disclaimer (wichtig, auf Wunsch von Ines)**: Sowohl vor der Berechnung (unter dem Platzhaltertext) als auch nach jeder Berechnung (unter dem Ergebnis) steht sichtbar, dass es sich um einen Richtwert ohne Gewähr handelt, keine rechtlich gesicherte Aussage und keine individuelle Beratung ersetzt. Zusätzlich in der Infobox ausführlicher erklärt. Das gilt für **alle** Ergebnisse, nicht nur für Länder mit Status "Entwurf"/"veraltet" – auch "final verkündete" Zahlen sind ein Rechenmodell, keine amtliche Auskunft.

## Layout

Gleiche Markenbasis wie [[02 Projekte/Fairbeamtet/BMI-Rechner.md|BMI-Rechner]], damit beide Tools als zusammengehörige „Rechner-Familie" wirken: Anton für Headlines/große Zahlen, Inter für Fließtext, Navy `#0B1E33` als Hero-/Ergebnis-Hintergrund, Pink/Magenta `#FF3F77` als Akzent- und CTA-Farbe, Blau `#0693E3` für Formularelemente. Gleiches Karten-/Stat-Kachel-Muster, gleiche Kontaktkarte am Ende (Platzhalter-Kreise statt Fotos, wie beim BMI-Rechner).

## Code

Version 2 – vollständig überarbeitet. Die Rechenlogik ist jetzt in drei Teile gegliedert: ein generisches additives Modell für 15 von 17 Dienstherren (inkl. Bayern, das sich nach Ortsklassen-Auflösung auf dasselbe additive Muster zurückführen lässt), plus eine eigene dreidimensionale Lookup-Tabelle nur für NRW. Besoldungsgruppe ist jetzt Pflichtfeld, Ortsklasse/Mietenstufe erscheinen konditional.

```html
<div class="fb-fz-rechner">
  <div class="fb-fz-hero">
    <div class="fb-fz-hero-watermark" aria-hidden="true">€</div>
    <div class="fb-fz-hero-inner">
      <p class="fb-fz-eyebrow">FAMILIENZUSCHLAG 2026</p>
      <h1>DEIN ZUSCHLAG.<br><span class="fb-fz-accent">JEDE BESOLDUNGSGRUPPE.</span></h1>
      <p class="fb-fz-intro">Bund oder Land, A 5 oder A 13, verheiratet oder nicht – der Familienzuschlag unterscheidet sich teils erheblich. Trag deine Situation ein, ich zeig dir deinen monatlichen Zuschlag mit Aufschlüsselung.</p>
      <a href="#fbFzForm" class="fb-fz-hero-button">Jetzt berechnen <span aria-hidden="true">&rarr;</span></a>
    </div>
  </div>

  <div class="fb-fz-stat-row">
    <div class="fb-fz-stat-tile">
      <div class="fb-fz-stat-number">17</div>
      <p>Dienstherren (Bund + 16 Länder), jeweils mit eigener Besoldungsregel seit der Föderalismusreform 2006.</p>
    </div>
    <div class="fb-fz-stat-tile fb-fz-stat-tile-accent">
      <div class="fb-fz-stat-number">A 3–A 16</div>
      <p>Besoldungsgruppe fließt in mehreren Ländern direkt in die Höhe des Zuschlags ein – wir rechnen das mit, nicht nur den Standardfall.</p>
    </div>
    <div class="fb-fz-stat-tile">
      <div class="fb-fz-stat-number">AB KIND 3</div>
      <p>In fast allen Bundesländern springt der Kinderanteil ab dem dritten Kind deutlich nach oben.</p>
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

          <label class="fb-fz-field">
            Besoldungsgruppe
            <select id="fbFzBesGr" required>
              <option value="A3">A 3</option>
              <option value="A4">A 4</option>
              <option value="A5">A 5</option>
              <option value="A6">A 6</option>
              <option value="A7">A 7</option>
              <option value="A8">A 8</option>
              <option value="A9" selected>A 9</option>
              <option value="A10">A 10</option>
              <option value="A11">A 11</option>
              <option value="A12">A 12</option>
              <option value="A13">A 13</option>
              <option value="A14">A 14</option>
              <option value="A15">A 15</option>
              <option value="A16">A 16</option>
              <option value="B">B-Besoldung / höherer Dienst</option>
            </select>
          </label>

          <label class="fb-fz-field fb-fz-field-hidden" id="fbFzOrtsklasseWrap">
            Ortsklasse (nach Wohnort, Bayern)
            <select id="fbFzOrtsklasse">
              <option value="I">I</option>
              <option value="II">II</option>
              <option value="III">III</option>
              <option value="IV">IV</option>
              <option value="V">V</option>
              <option value="VI">VI</option>
              <option value="VII">VII (z. B. München)</option>
            </select>
          </label>

          <label class="fb-fz-field fb-fz-field-hidden" id="fbFzMietenstufeWrap">
            Mietenstufe (nach Wohnort)
            <select id="fbFzMietenstufe">
              <option value="I">I</option>
              <option value="II">II</option>
              <option value="III">III</option>
              <option value="IV">IV</option>
              <option value="V">V</option>
              <option value="VI">VI</option>
              <option value="VII">VII</option>
            </select>
          </label>

          <label class="fb-fz-field fb-fz-field-checkbox">
            <input type="checkbox" id="fbFzVerheiratet">
            Verheiratet / verpartnert
          </label>

          <label class="fb-fz-field">
            Anzahl kindergeldberechtigter Kinder
            <input type="number" id="fbFzKinder" min="0" max="8" step="1" value="0" required>
          </label>
        </div>

        <button type="submit" class="fb-fz-button">Berechnen</button>
      </form>
    </div>

    <div class="fb-fz-result-card">
      <div class="fb-fz-placeholder" id="fbFzPlaceholder">
        <p>Wähl links dein Bundesland, deine Besoldungsgruppe und deine Familiensituation. Ich zeig dir deinen monatlichen Familienzuschlag.</p>
        <p class="fb-fz-disclaimer">Richtwert ohne Gewähr, keine rechtlich gesicherte Aussage.</p>
      </div>

      <div class="fb-fz-result" id="fbFzResult" hidden>
        <div class="fb-fz-status-badge" id="fbFzStatusBadge"></div>
        <div class="fb-fz-number"><span id="fbFzValue">0</span><span class="fb-fz-unit">€/Monat</span></div>
        <div class="fb-fz-breakdown" id="fbFzBreakdown"></div>
        <p class="fb-fz-kommentar" id="fbFzKommentar"></p>
        <div class="fb-fz-zusatz" id="fbFzZusatz" hidden></div>
        <p class="fb-fz-disclaimer">Richtwert ohne Gewähr. Keine rechtlich gesicherte Aussage und keine individuelle Beratung – dein konkreter Fall kann abweichen. Zwei Fälle sind hier nicht eingerechnet: Ist dein Partner/deine Partnerin ebenfalls im öffentlichen Dienst, gibt es den Ehe-/Partnerschaftsanteil meist nur anteilig (§ 40 BBesG). Den Kinderanteil bekommt zudem nur, wer das Kindergeld bezieht.</p>
      </div>
    </div>
  </div>

  <div class="fb-fz-infobox">
    <h2>So funktioniert der Familienzuschlag</h2>
    <p><strong>Wichtig, bevor du rechnest:</strong> Dieser Rechner liefert einen Richtwert, <strong>keine gesicherte oder rechtsverbindliche Aussage</strong>. Besoldungsrecht ändert sich laufend, enthält Sonderfälle, die hier nicht abgebildet sind, und einzelne Werte stammen noch aus dem Gesetzgebungsverfahren (Status "Entwurf" oder "Vorläufiger Abschlag", siehe Badge im Ergebnis) oder sind veraltet (Thüringen, siehe Hinweis). Zwei weitere Fälle fragen wir bewusst nicht ab: Ist dein Partner/deine Partnerin ebenfalls im öffentlichen Dienst, gibt es den Ehe-/Partnerschaftsanteil meist nur anteilig (§ 40 BBesG), und den Kinderanteil bekommt nur, wer das Kindergeld bezieht. Für eine verbindliche Berechnung wende dich an deine Bezügestelle oder lass dich von uns beraten.</p>
    <p>Der Familienzuschlag ergänzt deine Besoldung je nach Familienstand und Kinderzahl. Verheiratete oder verpartnerte Beamtinnen und Beamte erhalten einen Ehe-/Partnerschaftsanteil. Für jedes kindergeldberechtigte Kind kommt zusätzlich ein Kinderanteil hinzu, der ab dem dritten Kind in fast allen Bundesländern deutlich höher ausfällt. In mehreren Ländern (z. B. Baden-Württemberg, Niedersachsen, Bayern, NRW) hängt die genaue Höhe zusätzlich von deiner Besoldungsgruppe ab – niedrigere Gruppen bekommen teils einen Aufschlag, als Ausgleich für die niedrigere Grundbesoldung.</p>
    <p>Seit der Föderalismusreform 2006 legt jedes Bundesland seinen Familienzuschlag selbst im eigenen Landesbesoldungsgesetz fest. Bayern und Nordrhein-Westfalen koppeln die Höhe zusätzlich an deinen Wohnort (Ortsklasse bzw. Mietenstufe) – deshalb fragen wir das bei diesen beiden Ländern extra ab.</p>
    <p>Einige Länder zahlen zusätzlich einen separaten Familienergänzungszuschlag (z. B. Bremen) oder einen Ergänzenden Familienzuschlag für Sonderfälle (z. B. Berlin), die hier nicht in der Hauptsumme enthalten sind – wenn relevant, weisen wir das im Ergebnis gesondert aus. Alle Zahlen basieren auf den offiziellen Besoldungstabellen des dbb (Deutscher Beamtenbund), Stand November 2026 – <strong>ohne Gewähr für Richtigkeit, Vollständigkeit oder Aktualität</strong>. Mehr Hintergrund in unserem <a href="https://www.fairbeamtet.de/familienzuschlag-fuer-beamte/">ausführlichen Artikel zum Familienzuschlag</a>.</p>
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
  color: #1A1A1A !important;
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
  background: #0B1E33 !important;
  color: #fff !important;
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
  font-size: clamp(1.9rem, 7vw, 4rem);
  margin: 0 0 20px 0;
  line-height: 1.15;
  color: #fff !important;
  /* Verhindert den hässlichen Umbruch mitten im Wort ("BESOLDUNGSGR" / "UPPE.") auf
     schmalen Handy-Bildschirmen – lange Wörter springen jetzt komplett in die nächste
     Zeile statt an beliebiger Stelle zu brechen. */
  word-break: keep-all !important;
  overflow-wrap: normal !important;
  hyphens: none !important;
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
  background: #FF3F77 !important;
  color: #fff !important;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 30px;
  font-family: 'Inter', sans-serif;
  font-weight: 700;
}
.fb-fz-hero-button:hover {
  background: #D92F5F !important;
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
  background: #F4F6FA !important;
  border-radius: 14px;
  padding: 24px;
}
.fb-fz-stat-tile-accent {
  background: #FF3F77 !important;
  color: #fff !important;
}
.fb-fz-stat-tile-accent p {
  color: rgba(255,255,255,0.92) !important;
}
.fb-fz-stat-number {
  font-size: 1.8rem;
  line-height: 1;
  margin-bottom: 8px;
}
.fb-fz-stat-tile p {
  margin: 0;
  font-size: 0.92rem;
  line-height: 1.5;
  color: #1A1A1A !important;
}
.fb-fz-stat-tile .fb-fz-stat-number {
  color: #1A1A1A !important;
}
.fb-fz-stat-tile-accent .fb-fz-stat-number {
  color: #fff !important;
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
  background: #fff !important;
  border: 1px solid #E2E6EE;
  box-shadow: 0 10px 30px rgba(15,30,51,0.06);
}
.fb-fz-result-card {
  background: #0B1E33 !important;
  color: #fff !important;
  min-height: 220px;
  padding: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.fb-fz-result-card * {
  color: inherit !important;
}

.fb-fz-fields {
  display: grid;
  grid-template-columns: 1fr;
  gap: 18px;
  margin-bottom: 20px;
}
@media (min-width: 700px) {
  .fb-fz-fields {
    grid-template-columns: repeat(2, 1fr);
  }
}
.fb-fz-field {
  display: flex;
  flex-direction: column;
  gap: 6px;
  font-weight: 600;
  font-size: 0.95rem;
  min-width: 0;
  color: #1A1A1A !important;
}
/* Ohne diese Regel gewinnt ".fb-fz-field { display:flex }" gegen das native [hidden]-Verhalten
   (gleiche CSS-Spezifität, unsere Regel steht später) – Ortsklasse/Mietenstufe blieben dadurch
   für jedes Bundesland sichtbar, statt nur für Bayern bzw. NRW/Rheinland-Pfalz. */
.fb-fz-field[hidden],
.fb-fz-field.fb-fz-field-hidden {
  display: none !important;
}
.fb-fz-field-checkbox {
  flex-direction: row;
  align-items: center;
  gap: 10px;
}
/* !important auf allen größenrelevanten Eigenschaften, weil Theme-CSS (gleiches Muster wie
   beim BMI-Rechner, siehe dortige "Korrekturen nach erstem Praxistest") sonst Select-/Input-
   Felder auf die winzige Browser-Standardgröße zurückstutzt. */
.fb-fz-field select,
.fb-fz-field input[type="number"] {
  background: #fff !important;
  color: #1A1A1A !important;
  font-family: 'Inter', sans-serif !important;
  font-size: 1.05rem !important;
  line-height: 1.4 !important;
  padding: 14px 16px !important;
  min-height: 52px !important;
  border: 1px solid #D6DCE8 !important;
  border-radius: 10px !important;
  box-sizing: border-box !important;
  width: 100% !important;
  max-width: 100% !important;
  display: block !important;
}
/* Select-Felder brauchen eine eigene Regel: "-webkit-appearance: menulist" (native Darstellung)
   führt auf iOS Safari dazu, dass das Betriebssystem eine eigene, kompakte Mini-Box zeichnet
   und unser Padding/Mindesthöhe ignoriert – genau der "Felder zu klein"-Effekt auf dem Handy.
   Fix: native Darstellung komplett abschalten und einen eigenen Pfeil per Hintergrundbild zeichnen,
   dann greift unser Padding/Mindesthöhe zuverlässig auf jedem Gerät. */
.fb-fz-field select {
  -webkit-appearance: none !important;
  -moz-appearance: none !important;
  appearance: none !important;
  padding-right: 44px !important;
  /* SVG-Pfeil komplett URL-encodiert (keine rohen spitzen Klammern im Quelltext) – nachdem
     WordPress schon einmal "&&" im Script zerstört hat, soll hier nichts als HTML-Tag erkannt
     und vom Sicherheitsfilter herausgefiltert werden. */
  background-image: url("data:image/svg+xml,%3Csvg%20xmlns%3D%27http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%27%20width%3D%2714%27%20height%3D%279%27%20viewBox%3D%270%200%2014%209%27%3E%3Cpath%20d%3D%27M1%201L7%207L13%201%27%20stroke%3D%27%231A1A1A%27%20stroke-width%3D%272%27%20fill%3D%27none%27%20stroke-linecap%3D%27round%27%20stroke-linejoin%3D%27round%27%2F%3E%3C%2Fsvg%3E") !important;
  background-repeat: no-repeat !important;
  background-position: right 16px center !important;
  background-size: 14px 9px !important;
}
.fb-fz-field select:focus,
.fb-fz-field input:focus {
  outline: none !important;
  border-color: #0693E3 !important;
}
.fb-fz-field input[type="checkbox"] {
  width: 20px !important;
  height: 20px !important;
  min-height: 0 !important;
  accent-color: #0693E3 !important;
}

.fb-fz-button {
  font-family: 'Inter', sans-serif;
  background: #0693E3 !important;
  color: #fff !important;
  border: none;
  border-radius: 999px;
  padding: 16px 28px;
  font-size: 1.05rem;
  font-weight: 700;
  cursor: pointer;
  width: 100%;
}
.fb-fz-button:hover {
  background: #057AB0 !important;
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
.fb-fz-status-badge {
  display: inline-block;
  font-size: 0.7rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 4px 12px;
  border-radius: 999px;
  margin-bottom: 14px;
  background: rgba(255,255,255,0.15) !important;
  color: rgba(255,255,255,0.85) !important;
}
.fb-fz-status-badge.status-entwurf {
  background: rgba(255,200,0,0.2) !important;
  color: #FFD466 !important;
}
.fb-fz-status-badge.status-veraltet {
  background: rgba(255,63,119,0.25) !important;
  color: #FF9FBB !important;
}
.fb-fz-status-badge.status-abschlag {
  background: rgba(255,200,0,0.2) !important;
  color: #FFD466 !important;
}
.fb-fz-number {
  font-size: 4rem;
  line-height: 1;
  color: #fff !important;
}
.fb-fz-unit {
  font-size: 1.3rem;
  margin-left: 8px;
  color: #FF6FB5 !important;
}
.fb-fz-breakdown {
  margin: 16px 0;
  font-family: 'Inter', sans-serif;
  text-transform: none;
  font-size: 0.95rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.85) !important;
  text-align: left;
  display: inline-block;
}
.fb-fz-kommentar {
  font-size: 0.88rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.65) !important;
  margin-top: 8px;
}
.fb-fz-disclaimer {
  font-size: 0.78rem;
  line-height: 1.5;
  color: rgba(255,255,255,0.55) !important;
  margin-top: 14px;
  padding-top: 14px;
  border-top: 1px solid rgba(255,255,255,0.15);
}
.fb-fz-zusatz {
  margin-top: 16px;
  padding: 14px 16px;
  border-radius: 10px;
  background: rgba(255,255,255,0.08) !important;
  font-size: 0.85rem;
  line-height: 1.5;
  text-align: left;
  color: rgba(255,255,255,0.85) !important;
}

.fb-fz-infobox {
  background: #F4F6FA !important;
  padding: 32px;
  border-radius: 16px;
  line-height: 1.6;
}
.fb-fz-infobox h2 {
  margin-top: 0;
  font-size: 1.7rem;
  color: #1A1A1A !important;
}
.fb-fz-infobox p {
  color: #1A1A1A !important;
}
.fb-fz-infobox a {
  color: #0693E3 !important;
}

.fb-fz-contact-card {
  display: flex;
  gap: 24px;
  align-items: flex-start;
  background: #F4F6FA !important;
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
  background: #0693E3 !important;
  border: 3px solid #F4F6FA;
  margin-left: -16px;
}
.fb-fz-contact-photo:first-child {
  margin-left: 0;
  background: #9F4CFF !important;
}
.fb-fz-contact-photo:last-child {
  background: #FF3F77 !important;
}
.fb-fz-contact-label {
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  color: #0693E3 !important;
  margin: 0 0 4px 0;
}
.fb-fz-contact-text h2 {
  margin: 0 0 12px 0;
  font-size: 1.5rem;
  text-transform: none;
  color: #1A1A1A !important;
}
.fb-fz-contact-text p {
  margin: 0 0 16px 0;
  line-height: 1.6;
  color: #1A1A1A !important;
}
.fb-fz-cta-button {
  display: inline-block;
  background: #FF3F77 !important;
  color: #fff !important;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 28px;
  font-weight: 700;
  font-family: 'Inter', sans-serif;
}
.fb-fz-cta-button:hover {
  background: #D92F5F !important;
}
</style>

<script>
(function() {
  // ===== Datenbasis =====
  // Stand der Recherche: 13.11.2026, Primärquelle: offizielle dbb-Besoldungstabellen
  // (siehe Projektnotiz "Familienzuschlag-Rechner" für alle Einzelquellen).
  //
  // Struktur je additivem Bundesland:
  //   stufe1(besGr)      -> Ehe-/Partnerschaftsanteil (ggf. nach Besoldungsgruppenband)
  //   grund[4]           -> Grundsatz für Kind 1, Kind 2, Kind 3, Kind 4+ (Index 0-3)
  //   besGrDelta[besGr]  -> optionaler Aufschlag [d1,d2,d3,d4] auf die vier Kind-Sätze
  //   mietenstufeAddon   -> optional, nur Rheinland-Pfalz (Aufschlag ab Kind 3 nach Mietenstufe)
  //   ergaenzung(kinder) -> optional, separate Zusatzleistung (NICHT in der Summe enthalten)
  //   status: 'final' | 'entwurf' | 'veraltet'

  var FZ_ADDITIV = {
    bund: {
      name: 'Bund', gueltig: '01.05.2026', status: 'abschlag',
      stufe1: function() { return 181.36; },
      grund: [154.99, 154.99, 482.89, 482.89],
      besGrDelta: { A3: [5.37, 0, 26.84, 26.84], A4: [5.37, 0, 21.47, 21.47], A5: [5.37, 0, 16.10, 16.10] },
      // Faktencheck durch Sven, 13.11.2026: Grundlage ist die geltende Anlage V BBesG
      // (Stand 01.03.2024, 171,28 € / 146,38 € / 146,38 € / 456,06 €), darauf zwei Erhöhungen
      // (+3,0 % ab 01.04.2025, +2,8 % ab 01.05.2026, nach jedem Schritt gerundet) – daraus
      // ergeben sich rechnerisch exakt die hier hinterlegten Werte. ABER: Diese Erhöhung wird
      // nur als Abschlag gezahlt, unter dem Vorbehalt eines späteren Bundesalimentationsgesetzes.
      // Laut dbb gab es zum 27.10.2026 weder Kabinettsbeschluss noch abgestimmten Entwurf;
      // Minister Dobrindt kündigte am 02.11.2026 an, das Gesetz noch 2026 ins Kabinett zu bringen.
      // Ein früherer Referentenentwurf (April 2026) hatte den Ehe-/Partnerschaftsanteil ab 2026
      // sogar komplett gestrichen (nur noch Kinderanteile: 265 € für 1./2. Kind, 708 € für
      // 3. Kind laut oeffentlicher-dienst.org) – wurde vom BMI zurückgezogen und wird überarbeitet.
      // Die finale Regelung ist also offen, trotz der (vermutlich korrekten) Rechenschritte hier.
      hinweis: 'Diese Erhöhung ab Mai 2026 ist ein vorläufiger Abschlag, kein Gesetz. Das Bundesalimentationsgesetz dazu hat noch keinen Kabinettsbeschluss (Stand 13.11.2026). Ein früherer Entwurf hätte den Ehe-/Partnerschaftsanteil sogar komplett gestrichen. Die Zahl kann sich rückwirkend noch ändern.'
    },
    bw: {
      name: 'Baden-Württemberg', gueltig: '01.04.2026', status: 'entwurf',
      stufe1: function() { return 180.46; },
      grund: [157.78, 157.78, 989.17, 989.17],
      besGrDelta: {
        A7: [56.82, 0, 0, 0], A8: [56.82, 0, 0, 0], A9: [56.82, 0, 0, 0], A10: [56.82, 0, 0, 0],
        A11: [28.41, 0, 0, 0], A12: [28.41, 0, 0, 0], A13: [28.41, 0, 0, 0]
      },
      hinweis: 'Der zusätzliche Familienergänzungszuschlag nach Erfahrungsstufe des Grundgehalts ist hier NICHT eingerechnet (würde ein eigenes Eingabefeld "Erfahrungsstufe" erfordern, nur für dieses Bundesland).'
    },
    be: {
      name: 'Berlin', gueltig: '01.04.2026', status: 'final',
      stufe1: function() { return 0; },
      grund: [148.44, 148.44, 819.76, 678.99],
      besGrDelta: {},
      hinweis: 'Ein Ergänzender Familienzuschlag nach § 40a BBesG BE für Sonderfälle (reduzierter regulärer Zuschlag) ist hier nicht eingerechnet.'
    },
    bb: {
      name: 'Brandenburg', gueltig: '01.01.2026', status: 'final',
      stufe1: function() { return 0; },
      grund: [377.16, 377.16, 888.39, 888.39],
      besGrDelta: {},
      hinweis: 'Brandenburg zahlt keinen Ehe-/Partnerschaftsanteil, nur den kinderbezogenen Teil.'
    },
    hb: {
      name: 'Bremen', gueltig: '01.04.2026', status: 'entwurf',
      stufe1: function(besGr) { return ['A5', 'A6', 'A7', 'A8'].indexOf(besGr) !== -1 ? 166.18 : 174.54; },
      grund: [265.85, 265.85, 610.60, 587.27],
      besGrDelta: { A5: [18.00, 0, 40.00, 40.00] },
      hinweis: null,
      ergaenzung: function(kinder) {
        var s = 0;
        for (var i = 1; i <= kinder; i++) { s += (i <= 3) ? 375.00 : 385.00; }
        return s;
      },
      ergaenzungLabel: 'Familienergänzungszuschlag (§ 35a BremBesG), separate Leistung'
    },
    hh: {
      name: 'Hamburg', gueltig: '01.04.2026', status: 'final',
      stufe1: function() { return 165.84; },
      grund: [193.14, 193.14, 635.00, 635.00],
      besGrDelta: { A3: [5.11, 0, 25.56, 25.56], A4: [5.11, 0, 20.45, 20.45], A5: [5.11, 0, 15.34, 15.34] },
      hinweis: null
    },
    he: {
      name: 'Hessen', gueltig: '01.07.2026', status: 'final',
      stufe1: function() { return 177.30; },
      grund: [360.57, 360.57, 831.08, 831.08],
      besGrDelta: {},
      hinweis: null
    },
    mv: {
      name: 'Mecklenburg-Vorpommern', gueltig: '01.04.2026', status: 'final',
      stufe1: function() { return 164.77; },
      grund: [198.83, 198.83, 820.00, 820.00],
      besGrDelta: { A4: [36.17, 36.17, 0, 0], A5: [31.17, 31.17, 0, 0], A6: [16.17, 16.17, 0, 0] },
      hinweis: null
    },
    ni: {
      name: 'Niedersachsen', gueltig: '01.04.2026', status: 'final',
      stufe1: function(besGr) { return ['A5', 'A6', 'A7', 'A8'].indexOf(besGr) !== -1 ? 162.26 : 170.36; },
      grund: [145.61, 145.61, 512.37, 512.37],
      besGrDelta: { A5: [100, 100, 0, 0], A6: [100, 100, 0, 0], A7: [100, 100, 0, 0], A8: [100, 100, 0, 0], A9: [100, 100, 0, 0] },
      hinweis: 'Die Erhöhung für A5–A9 gilt nur in der Laufbahngruppe 1 – wird hier pauschal angenommen.'
    },
    rp: {
      name: 'Rheinland-Pfalz', gueltig: '01.04.2026', status: 'final',
      stufe1: function() { return 88.03; },
      grund: [246.97, 246.97, 726.00, 726.00],
      besGrDelta: { A5: [5.32, 15.98, 0, 0] },
      mietenstufeAddon: { V: 19.00, VI: 43.00, VII: 68.00 },
      hinweis: null
    },
    sl: {
      name: 'Saarland', gueltig: '01.04.2026', status: 'final',
      stufe1: function() { return 164.48; },
      grund: [165.31, 165.31, 781.68, 781.68],
      besGrDelta: { A4: [17.91, 0, 71.65, 71.65], A5: [17.91, 0, 47.77, 47.77], A6: [17.91, 0, 23.88, 23.88] },
      hinweis: null
    },
    sn: {
      name: 'Sachsen', gueltig: '01.04.2026', status: 'final',
      stufe1: function() { return 279.58; },
      grund: [279.58, 279.58, 795.41, 795.41],
      besGrDelta: { A5: [5.11, 0, 20.45, 20.45] },
      hinweis: null
    },
    st: {
      name: 'Sachsen-Anhalt', gueltig: '01.04.2026', status: 'final',
      stufe1: function() { return 169.04; },
      grund: [184.85, 184.85, 818.98, 818.98],
      besGrDelta: { A5: [6.69, 20.11, 20.11, 20.11] },
      hinweis: null
    },
    sh: {
      name: 'Schleswig-Holstein', gueltig: '01.01.2026', status: 'final',
      stufe1: function() { return 176.24; },
      grund: [199.85, 199.85, 516.48, 516.48],
      besGrDelta: {},
      hinweis: null
    },
    th: {
      name: 'Thüringen', gueltig: '01.02.2025', status: 'veraltet',
      stufe1: function() { return 177.25; },
      grund: [149.16, 202.75, 301.34, 803.23],
      besGrDelta: {},
      hinweis: 'Keine 2026er-Anpassung gefunden – Zahlen mit Stand Februar 2025, vor Veröffentlichung prüfen.'
    }
  };

  // Bayern: Ortsklassen-Tabelle (Anlage 5 BayBesG, dbb-Stand 01.10.2026) wird zur Laufzeit
  // in dieselbe additive Struktur wie oben übersetzt (siehe bayernConfig()).
  var BY_ORTSKLASSEN = {
    I:   { stufeV: 87.51,  stufe1: 346.98, stufe2: 506.90, kind3: 495.64, weiteres: 593.37 },
    II:  { stufeV: 87.51,  stufe1: 346.98, stufe2: 506.90, kind3: 495.64, weiteres: 593.37 },
    III: { stufeV: 87.51,  stufe1: 346.98, stufe2: 542.58, kind3: 510.51, weiteres: 640.81 },
    IV:  { stufeV: 87.51,  stufe1: 370.73, stufe2: 578.24, kind3: 525.84, weiteres: 688.72 },
    V:   { stufeV: 112.50, stufe1: 394.46, stufe2: 613.90, kind3: 541.61, weiteres: 737.05 },
    VI:  { stufeV: 137.50, stufe1: 418.20, stufe2: 693.03, kind3: 557.87, weiteres: 785.88 },
    VII: { stufeV: 170.26, stufe1: 546.06, stufe2: 784.86, kind3: 574.59, weiteres: 835.19 }
  };
  var BY_BESGR_ORDER = ['A3', 'A4', 'A5', 'A6', 'A7', 'A8', 'A9', 'A10'];
  var BY_ERHOEHUNG = {
    I:   [35.15, 31.12, 30.05, 27.96, 24.59, 22.34, 18.09, 10.91],
    II:  [37.26, 34.96, 33.76, 31.40, 27.63, 25.09, 20.31, 12.25],
    III: [41.40, 38.85, 37.51, 34.88, 30.70, 27.87, 22.55, 13.60],
    IV:  [45.99, 43.15, 41.67, 38.73, 34.11, 30.97, 25.06, 15.11],
    V:   [50.54, 47.41, 45.79, 42.57, 37.47, 34.03, 27.52, 16.61],
    VI:  [54.92, 51.52, 49.75, 46.27, 40.72, 36.97, 29.91, 18.06],
    VII: [60.35, 56.61, 54.68, 50.83, 44.74, 40.62, 32.87, 19.83]
  };

  function bayernConfig(ortsklasse) {
    var o = BY_ORTSKLASSEN[ortsklasse];
    var besGrDelta = {};
    var bgIdx = BY_BESGR_ORDER.indexOf;
    BY_BESGR_ORDER.forEach(function(bg, i) {
      var v = BY_ERHOEHUNG[ortsklasse][i];
      besGrDelta[bg] = [v, v, v, v];
    });
    return {
      name: 'Bayern (Ortsklasse ' + ortsklasse + ')',
      gueltig: '01.10.2026',
      status: 'entwurf',
      stufe1: function() { return o.stufeV; },
      grund: [o.stufe1 - o.stufeV, o.stufe2 - o.stufe1, o.kind3, o.weiteres],
      besGrDelta: besGrDelta,
      hinweis: 'Stand 01.10.2026 laut dbb-Besoldungstabelle (neuer als der amtliche Gesetzestext auf gesetze-bayern.de, der zum Rechercheabruf noch 01.02.2025 zeigte) – vor Launch gegenprüfen.'
    };
  }

  // NRW: echte dreidimensionale Lookup-Tabelle (Besoldungsgruppenband x Mietenstufe x Kinderzahl),
  // keine Addition möglich. Quelle: amtliches PDF recht.nrw.de, Anhang 8 LBesG NRW, gültig 01.04.2026.
  var NW_STUFE1 = { A5: 169.26, A6: 169.26, A7: 167.26, A8: 167.26 }; // sonst 173.50 (übrige)
  var NW_STUFEN = {
    A5A6: {
      stufe2: [323.89, 323.89, 373.17, 518.14, 650.94, 793.75, 954.44],
      stufe3: [737.09, 880.30, 1027.88, 1199.36, 1361.94, 1529.08, 1724.50],
      stufe4: [1450.50, 1615.85, 1789.38, 1991.40, 2176.88, 2373.13, 2600.78],
      stufe5: [2169.15, 2359.21, 2559.84, 2789.90, 2999.21, 3237.91, 3498.95],
      ab5: [760.89, 788.82, 819.69, 851.89, 879.53, 928.98, 968.42]
    },
    A7A8: {
      stufe2: [320.07, 320.07, 369.36, 514.32, 647.13, 769.94, 950.62],
      stufe3: [731.44, 874.66, 1022.24, 1193.72, 1356.29, 1523.45, 1718.87],
      stufe4: [1439.21, 1604.55, 1778.08, 1980.11, 2165.58, 2361.84, 2588.49],
      stufe5: [2152.20, 2342.26, 2542.88, 2772.95, 2982.26, 3220.96, 3482.00],
      ab5: [755.23, 783.16, 814.02, 846.23, 873.87, 923.32, 962.70]
    },
    uebrige: {
      stufe2: [324.52, 324.52, 373.81, 518.76, 651.57, 794.39, 955.05],
      stufe3: [734.08, 877.30, 1024.87, 1196.36, 1358.93, 1526.09, 1721.50],
      stufe4: [1436.24, 1601.59, 1775.12, 1977.14, 2162.61, 2358.88, 2586.52],
      stufe5: [2143.84, 2333.59, 2534.32, 2784.39, 2973.69, 3212.40, 3473.44],
      ab5: [749.64, 777.56, 808.43, 840.64, 868.27, 917.73, 957.16]
    }
  };
  var MIETENSTUFEN_INDEX = { I: 0, II: 1, III: 2, IV: 3, V: 4, VI: 5, VII: 6 };

  function nwBand(besGr) {
    if (besGr === 'A5' || besGr === 'A6') return 'A5A6';
    if (besGr === 'A7' || besGr === 'A8') return 'A7A8';
    return 'uebrige';
  }

  function berechneNRW(besGr, verheiratet, kinder, mietenstufe) {
    var band = nwBand(besGr);
    var idx = MIETENSTUFEN_INDEX[mietenstufe];
    var tab = NW_STUFEN[band];
    var zeilen = [];
    var summe;

    if (kinder === 0) {
      var stufe1 = NW_STUFE1[besGr] !== undefined ? NW_STUFE1[besGr] : 173.50;
      summe = verheiratet ? stufe1 : 0;
      if (verheiratet) zeilen.push('Ehezuschlag (Stufe 1): ' + formatEuro(stufe1) + ' €');
    } else if (kinder <= 4) {
      var key = ['stufe2', 'stufe3', 'stufe4', 'stufe5'][kinder - 1];
      summe = tab[key][idx];
      zeilen.push('Gesamtbetrag für ' + kinder + ' Kind' + (kinder === 1 ? '' : 'er') + ' (Mietenstufe ' + mietenstufe + '): ' + formatEuro(summe) + ' €');
    } else {
      summe = tab.stufe5[idx] + (kinder - 4) * tab.ab5[idx];
      zeilen.push('Gesamtbetrag für 4 Kinder (Mietenstufe ' + mietenstufe + '): ' + formatEuro(tab.stufe5[idx]) + ' €');
      zeilen.push('+ ' + (kinder - 4) + ' weitere Kind(er) à ' + formatEuro(tab.ab5[idx]) + ' €: ' + formatEuro((kinder - 4) * tab.ab5[idx]) + ' €');
    }

    // Zusatz A5: +8,65 € für das erste Kind, ab dem zweiten Kind je +25,67 €
    if (besGr === 'A5') {
      if (kinder >= 1) {
        var zusatzA5 = 8.65 + Math.max(0, kinder - 1) * 25.67;
        summe += zusatzA5;
        zeilen.push('Zuschlag Besoldungsgruppe A 5: +' + formatEuro(zusatzA5) + ' €');
      }
    }

    return { summe: summe, zeilen: zeilen };
  }

  // ===== Generische additive Berechnung =====
  function berechneAdditiv(cfg, besGr, verheiratet, kinder, mietenstufe) {
    var stufe1 = cfg.stufe1(besGr);
    var delta = [0, 0, 0, 0];
    if (cfg.besGrDelta) {
      if (cfg.besGrDelta[besGr]) {
        delta = cfg.besGrDelta[besGr];
      }
    }
    var zeilen = [];
    var ehe = verheiratet ? stufe1 : 0;
    if (verheiratet) zeilen.push('Ehe-/Partnerschaftsanteil: ' + formatEuro(ehe) + ' €');

    var kinderSumme = 0;
    var besGrZuschlagAngewendet = false;
    var mietenstufeZuschlagAngewendet = false;
    for (var i = 1; i <= kinder; i++) {
      var idx = Math.min(i - 1, 3);
      var rate = cfg.grund[idx] + delta[idx];
      if (delta[idx]) { besGrZuschlagAngewendet = true; }
      if (cfg.mietenstufeAddon) {
        if (idx >= 2) {
          if (mietenstufe) {
            if (cfg.mietenstufeAddon[mietenstufe]) {
              rate += cfg.mietenstufeAddon[mietenstufe];
              mietenstufeZuschlagAngewendet = true;
            }
          }
        }
      }
      kinderSumme += rate;
    }
    if (kinder > 0) {
      // Zusatz nur erwähnen, wenn tatsächlich etwas eingerechnet wurde – sonst wäre die Angabe
      // irreführend (z. B. beim Bund in A 9: da greift keiner der beiden Zuschläge, siehe
      // Faktencheck 13.11.2026).
      var zusaetze = [];
      if (besGrZuschlagAngewendet) { zusaetze.push('Besoldungsgruppen-Zuschlag'); }
      if (mietenstufeZuschlagAngewendet) { zusaetze.push('Mietenstufen-Zuschlag'); }
      var zusatzText = zusaetze.length ? ' (inkl. ' + zusaetze.join(' und ') + ')' : '';
      zeilen.push('Kinderanteil für ' + kinder + ' Kind' + (kinder === 1 ? '' : 'er') + zusatzText + ': ' + formatEuro(kinderSumme) + ' €');
    }
    if (kinder === 0) {
      if (!verheiratet) {
        zeilen.push('Ohne Ehe-/Partnerschaft und ohne Kinder entsteht kein Familienzuschlag.');
      }
    }

    return { summe: ehe + kinderSumme, zeilen: zeilen };
  }

  function formatEuro(betrag) {
    return betrag.toLocaleString('de-DE', { minimumFractionDigits: 2, maximumFractionDigits: 2 });
  }

  // ===== UI =====
  var landSelect = document.getElementById('fbFzLand');
  var ortsklasseWrap = document.getElementById('fbFzOrtsklasseWrap');
  var mietenstufeWrap = document.getElementById('fbFzMietenstufeWrap');
  var form = document.getElementById('fbFzForm');
  var placeholder = document.getElementById('fbFzPlaceholder');
  var result = document.getElementById('fbFzResult');
  var statusBadge = document.getElementById('fbFzStatusBadge');
  var valueEl = document.getElementById('fbFzValue');
  var breakdownEl = document.getElementById('fbFzBreakdown');
  var kommentarEl = document.getElementById('fbFzKommentar');
  var zusatzEl = document.getElementById('fbFzZusatz');

  // Versteckt per CSS-Klasse statt per [hidden]-Attribut – robuster, falls irgendein
  // Plugin/Theme/Sanitizer auf der Seite Attribute anders behandelt als Klassen.
  // Ortsklasse gilt nur für Bayern, Mietenstufe nur für NRW (zwingend) und Rheinland-Pfalz
  // (nur für den Kind-3+-Aufschlag). Für alle anderen 15 Dienstherren, inkl. Bund, bleiben
  // beide Felder versteckt.
  function updateConditionalFields() {
    var land = landSelect.value;
    if (land === 'by') {
      ortsklasseWrap.classList.remove('fb-fz-field-hidden');
    } else {
      ortsklasseWrap.classList.add('fb-fz-field-hidden');
    }
    if (land === 'nw' || land === 'rp') {
      mietenstufeWrap.classList.remove('fb-fz-field-hidden');
    } else {
      mietenstufeWrap.classList.add('fb-fz-field-hidden');
    }
  }
  landSelect.addEventListener('change', updateConditionalFields);
  updateConditionalFields();

  var STATUS_LABEL = {
    final: 'Final verkündet',
    entwurf: 'Entwurf, noch nicht verkündet',
    veraltet: 'Veraltete Daten – prüfen',
    abschlag: 'Vorläufiger Abschlag, kein Gesetz'
  };

  form.addEventListener('submit', function(e) {
    e.preventDefault();

    var land = landSelect.value;
    var besGr = document.getElementById('fbFzBesGr').value;
    var verheiratet = document.getElementById('fbFzVerheiratet').checked;
    var kinder = parseInt(document.getElementById('fbFzKinder').value, 10) || 0;
    var ortsklasse = document.getElementById('fbFzOrtsklasse').value;
    var mietenstufe = document.getElementById('fbFzMietenstufe').value;

    var cfg, berechnung, gueltig, status, name, zusatzHinweis = null, zusatzBetrag = null, zusatzLabel = null;

    if (land === 'nw') {
      berechnung = berechneNRW(besGr, verheiratet, kinder, mietenstufe);
      name = 'Nordrhein-Westfalen (Mietenstufe ' + mietenstufe + ')';
      gueltig = '01.04.2026';
      status = 'final';
    } else if (land === 'by') {
      cfg = bayernConfig(ortsklasse);
      berechnung = berechneAdditiv(cfg, besGr, verheiratet, kinder, null);
      name = cfg.name;
      gueltig = cfg.gueltig;
      status = cfg.status;
      zusatzHinweis = cfg.hinweis;
    } else {
      cfg = FZ_ADDITIV[land];
      berechnung = berechneAdditiv(cfg, besGr, verheiratet, kinder, mietenstufe);
      name = cfg.name;
      gueltig = cfg.gueltig;
      status = cfg.status;
      zusatzHinweis = cfg.hinweis;
      if (cfg.ergaenzung) {
        zusatzBetrag = cfg.ergaenzung(kinder);
        zusatzLabel = cfg.ergaenzungLabel;
      }
    }

    valueEl.textContent = formatEuro(berechnung.summe);
    breakdownEl.innerHTML = berechnung.zeilen.map(function(z) { return '<div>' + z + '</div>'; }).join('');

    statusBadge.textContent = STATUS_LABEL[status] || status;
    statusBadge.className = 'fb-fz-status-badge' + (status !== 'final' ? ' status-' + status : '');

    var kommentar = name + ', gültig ab ' + gueltig + '.';
    kommentarEl.textContent = kommentar;

    if (zusatzBetrag !== null || zusatzHinweis) {
      var zusatzHtml = '';
      if (zusatzBetrag !== null) {
        zusatzHtml += '<strong>+ ' + formatEuro(zusatzBetrag) + ' € ' + zusatzLabel + '</strong><br>Diese Leistung ist NICHT in der Summe oben enthalten, wird aber zusätzlich gezahlt.';
      }
      if (zusatzHinweis) {
        zusatzHtml += (zusatzHtml ? '<br><br>' : '') + zusatzHinweis;
      }
      zusatzEl.innerHTML = zusatzHtml;
      zusatzEl.hidden = false;
    } else {
      zusatzEl.hidden = true;
    }

    placeholder.hidden = true;
    result.hidden = false;
  });
})();
</script>
```


## Hinweise zur Einbindung

- Gleiche Schrift-/Farb-Basis wie [[02 Projekte/Fairbeamtet/BMI-Rechner.md|BMI-Rechner]] – siehe dort zu DSGVO-Pflicht beim Self-Hosting der Schrift vor Go-Live.
- Kontaktkarte mit Foto-Platzhaltern, analog zum BMI-Rechner – echte Fotos aus [[00 Kontext/Fairbeamtet/Team.md|Team]] einsetzen, sobald verfügbar.
- CTA-Links sind Platzhalter (`#`) – echte URL zur Beratungs-/Kontaktseite einsetzen.
- Die Datenstruktur (`FZ_ADDITIV`, `BY_ORTSKLASSEN`/`BY_ERHOEHUNG`, `NW_STUFEN`) ist bewusst so gebaut, dass sie sich künftig leicht aktualisieren lässt (ein Objekt pro Bundesland, bzw. eine Tabelle pro Sonderfall) – das deckt sich mit der in [[02 Projekte/Fairbeamtet/Eigener Gehaltsrechner.md|Eigener Gehaltsrechner]] geforderten zentralen Datenpflege statt händischer Einzelpflege pro Seite.
- Der Rechner deckt jetzt alle 17 Dienstherren mit Zahlenausgabe ab (keine Blockierung mehr wie in Version 1) – dafür muss vor Launch die Datenqualität der "Entwurf"- und "veraltet"-Fälle (Baden-Württemberg, Bayern, Bremen, Thüringen) zwingend gegengeprüft werden, siehe "Bekannte Unsicherheiten" oben.
- Bewusst nicht abgebildet (zu komplex für ein MVP-Formular mit vertretbarer Feldzahl): Baden-Württembergs Erfahrungsstufen-abhängiger Familienergänzungszuschlag, Berlins Ergänzender Familienzuschlag nach § 40a. Beide werden im Ergebnis als Hinweistext angezeigt, aber nicht berechnet.
- **Bug gefunden und behoben (13.11.2026):** Beim ersten Einfügen in ein WordPress-"Individuelles HTML"-Feld wurden zwei von fünf `&&`-Verknüpfungen im Script zu `&#038;&#038;` verändert (vermutlich durch Encoding beim Einfügen/Speichern) – das hat das gesamte Script mit einem Syntaxfehler zum Abbruch gebracht, ohne dass der BMI-Rechner (der kein `&&` enthält) betroffen war. Der Code enthält jetzt **kein `&&` mehr** (durch verschachtelte `if`-Abfragen ersetzt), damit das nicht wieder passieren kann, unabhängig von der genauen Ursache. **Beim erneuten Einbinden: den kompletten alten Code im HTML-Feld löschen und durch die aktuelle Version unten ersetzen**, nicht nur die betroffenen Zeilen patchen.
- **Zweiter Bug gefunden und behoben (13.11.2026):** Nach dem ersten Fix liefen die Eingabefelder (Dropdowns/Zahlenfeld) zu klein, weil Theme-CSS der Live-Seite die Select-/Input-Größe überschrieben hat – derselbe Bug-Typ wie die unlesbare Hero-Schrift beim BMI-Rechner. Fix: alle größenrelevanten CSS-Eigenschaften (Padding, Schriftgröße, Mindesthöhe, Breite) jetzt mit `!important`, zusätzlich das Eingabefelder-Raster standardmäßig einspaltig (vorher zweispaltig, was die Felder bei schmaleren Theme-Containern zusätzlich gestaucht hat) und erst ab 700px Breite zweispaltig.

## Nächste Schritte

- [ ] Thüringen 2026 nachrecherchieren (aktuell nur Stand Februar 2025 verfügbar)
- [ ] Die drei "Entwurf"-Länder (Baden-Württemberg, Bayern, Bremen) gegen die inzwischen verkündeten Gesetzblätter prüfen
- [ ] Mit Sven abstimmen: fachliche Freigabe der Zahlen, Platzierung auf der Seite (eigenständige Rechner-Seite vs. Einbindung im bestehenden Artikel), Umgang mit den bewusst ausgeklammerten Sonderfällen (BW-Erfahrungsstufe, Berlin § 40a)
- [ ] Echten Link zur Beratungs-/Kontaktseite einsetzen
- [ ] Jährlichen Update-Prozess für die Zahlen festlegen (mehrere Länder passen zum 1. April an, der Bund zum 1. Mai, einzelne zum 1. Januar/Juli)
- [ ] Vor Launch: Testdurchlauf mit mehreren Kombinationen (insbesondere NRW/Bayern mit verschiedenen Ortsklassen/Mietenstufen und Besoldungsgruppen) gegen die Tabellen in diesem Dokument
- [ ] Erst nach Freigabe: live schalten
