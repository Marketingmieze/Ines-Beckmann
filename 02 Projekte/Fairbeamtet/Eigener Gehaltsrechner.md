---
tags: [projekt, fairbeamtet]
status: entwurf
erstellt: 2026-11-10
---

# Eigener Gehaltsrechner – Analyse & Konzept

## Ziel

Prüfen, ob und wie fairbeamtet.de einen eigenen Gehalts-/Besoldungsrechner baut, als Antwort auf den Haupttraffic-Treiber von [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|einfachverbeamtet.de]]. Ggf. mit Verbesserungen gegenüber dem Vorbild und klaren Handlungsaufforderungen für den Nutzer.

## Status

Entwurf – Konzept steht, noch keine Umsetzung/Entwicklung beauftragt.

## Ausgangslage: Warum jetzt

Laut Wettbewerber-Steckbrief vom 10.11.2026 (Sven, Ahrefs-Daten, siehe [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]]):

- einfachverbeamtet.de ist in 5 Monaten von 0 auf ~6.600 Besucher/Monat gewachsen, DR 8, ohne echten Linkaufbau, ohne Werbung.
- Der **Gehaltsrechner allein bringt ~1.672 Besucher/Monat – rund ein Viertel des gesamten Traffics der Seite.** Kein anderer Einzelinhalt kommt annähernd heran (nächstgrößte Seite: Besoldung Lehrer Bayern mit 760).
- Übergeordnete Hypothese aus der Analyse: „Ein funktionierender Rechner zieht mehr Besucher als jede Textseite."
- Das deckt sich mit [[04 Ressourcen/Googles No. 1/Originaere Daten Tools und Experience.md|Originäre Daten, Tools und Experience]] (Hebel 4 von 10): Google zählt Aufwand in Funktionalität explizit als Content-Qualität, nennt im Rater-Guideline-Beispiel ausdrücklich einen BMI-Rechner als „Highest Quality"-Vorbild bei YMYL-Themen, und die Best-Practice-Empfehlung dort lautet bereits seit 27.09.2026 wörtlich: „Rechner bauen, nicht nur Texte schreiben. Ein Beihilferechner nach Bundesland, ein Beitragsrechner für Anwärter, ein Vergleichsrechner Beihilfe plus PKV gegen GKV."

Das ist also kein neuer Gedanke, sondern ein bereits dokumentierter, jetzt durch den Konkurrenten mit echten Zahlen belegter Hebel.

## Der Rechner von einfachverbeamtet.de – Bestandsaufnahme

URL: https://www.einfachverbeamtet.de/gehaltsrechner/ (abgerufen 10.11.2026, Inhalte teils JS-gerendert, Formularfelder selbst nicht vollständig auslesbar)

**Eingaben (beworben):**
- Bundesland (alle 16)
- Besoldungsgruppe A6–A16 inkl. aller Stufen
- Familienstand, Kinderzuschlag
- Dienstjahre
- Dienstunfähigkeit als Szenario

**Ausgaben – das ist der eigentliche Clou, nicht nur „Gehalt berechnen":**
- Brutto- und Nettogehalt
- Pension nach Dienstjahren
- **Pensionslücke zum Aktivgehalt**
- Dienstunfähigkeits-Pension
- **Versorgungslücke im Alter**
- Familien- und Kinderzuschlag
- **Nötige ETF-Sparrate**, um die Lücke zu schließen
- Bundesland-Vergleich

Der Rechner ist also kein reiner Gehaltsrechner, sondern ein **Lücken-Rechner mit eingebauter Verkaufslogik**: Er zeigt nicht nur „was verdienst du", sondern „wo tut es weh" (Pensionslücke, Versorgungslücke) und liefert direkt die Zahl, die eine Vorsorgelösung rechtfertigt (ETF-Sparrate). Das Ergebnis ist strukturell schon der Beratungsanlass.

**Rahmung auf der Seite:**
- Hero: „Dein Gehalt, deine Pension und deine Versorgungslücke – in wenigen Sekunden berechnet." Subtext stellt explizit „transparent, individuell und ohne Anmeldung" heraus.
- Trust-Signale direkt über dem Rechner: „100 % kostenlos", „Ohne Anmeldung", „Ergebnis in Sekunden", „Alle 16 Bundesländer", „Aktuelle Besoldungstabellen 2026".
- Darunter Zielgruppen-Kacheln (Lehrer, Polizei, Verwaltung, Finanzbeamte, Anwärter, Pensionsnahe, Familien) – jeder Besucher findet sich wieder.
- Social Proof: 5,0★ auf Basis von 67 Google-Bewertungen, ca. 19 Testimonials mit Namen und Beratern.
- **Zwei CTAs nach dem Rechner:** „Jetzt kostenlose Beratung buchen" und „Absicherung als Beamter prüfen" – beide auf dieselbe Kontaktseite (/kontakt/), kein Lead-Formular direkt im Rechner (kein E-Mail-Gate, keine Anmeldung nötig für das Ergebnis).
- Footer verlinkt auf Webinar-Termine, Blog, Forum, Glossar – das Ökosystem drumherum ist breit angelegt.

**Was fehlt/unklar bleibt (von außen nicht prüfbar ohne Interaktion):**
- Keine sichtbaren Quellenangaben/Stand-Datum einzelner Besoldungstabellen direkt im Rechner-UI (nur pauschal „Besoldungstabellen 2026" im Marketing-Text).
- Kein PDF-Export oder Ergebnis-Versand sichtbar in der statischen Ansicht.
- Methodik der ETF-Sparraten-Berechnung (Zinsannahme, Inflationsannahme) nicht transparent erkennbar.

## Einordnung: Passt das zu fairbeamtet?

Kein Markenkonflikt, im Gegenteil – ICP und Angebot passen direkt:

- [[00 Kontext/Fairbeamtet/ICP.md|ICP]]: Kernzielgruppe Beamte/Anwärter/Referendare, Ziel ist „eine Versicherungslösung, die wirklich zur Lebenssituation passt" statt der billigsten auf dem Papier.
- [[00 Kontext/Fairbeamtet/Angebot.md|Angebot]]: PKV, Vorsorge, Sachversicherungen, Risikovoranfrage – persönliche Betreuung statt anonymer Tarifvergleich.

Ein Rechner, der eine Versorgungslücke sichtbar macht und direkt zur persönlichen Beratung führt, ist strukturell identisch zum eigenen Geschäftsmodell: nicht „billigster Tarif", sondern „deine Lücke, deine passende Lösung". Das unterscheidet sich vom einfachverbeamtet-Modell nur in der Tonalität, nicht im Mechanismus.

## Empfehlung: Eigener Rechner mit Verbesserungen

### 1. Nicht 1:1 kopieren, sondern den fairbeamtet-Winkel nehmen

Statt eines reinen Gehalts-/Pensionsrechners (das Themenfeld, in dem der Konkurrent bereits 5 Monate Vorsprung und ~130 rankende Seiten hat) einen Rechner bauen, der auf fairbeamtets tatsächliche Kernkompetenz einzahlt:

- **Beihilfe- und PKV-Rechner**: Beihilfesatz nach Bundesland/Laufbahn × PKV-Beitrag grob × Vergleich zur GKV – genau die Kombination, die in [[04 Ressourcen/Googles No. 1/Originaere Daten Tools und Experience.md|Originäre Daten, Tools und Experience]] schon als Vorschlag steht und die fachlich zu PKV und Beihilfe passt statt zu reinem Besoldungsrecht.
- Gehaltsrechner als Einstiegsmodul trotzdem sinnvoll, weil er die Suchnachfrage abdeckt (Vol. zeigt sich im Konkurrenz-Traffic), aber als **Baustein eines größeren Vorsorge-/Lücken-Rechners**, nicht als Solo-Thema wie beim Wettbewerber.

### 2. Verbesserungen gegenüber dem Vorbild

- **Quellentransparenz direkt im Tool**: Stand der Besoldungstabelle, Paragraf/Gesetzesstelle, Datum der letzten Aktualisierung sichtbar im Rechner selbst, nicht nur im Marketingtext. Deckt sich mit der Vault-Regel zu aktuellen Werten und mit Googles „Accuracy"-Kriterium – und ist eine Lücke, die der Konkurrent (soweit von außen sichtbar) offenlässt.
- **Berechnungsmethodik offenlegen** (z. B. bei der ETF-Sparraten-Logik: welche Rendite-/Inflationsannahme), wo der Wettbewerber intransparent bleibt. Schafft Vertrauen und ist ein Unterscheidungsmerkmal, das zur „ehrliche Beratung statt Verkaufsdruck"-Positionierung passt.
- **Ergebnis als PDF/Download oder Versand per E-Mail** anbieten – das wäre zugleich ein legitimer, nutzerwert-first Lead-Mechanismus (Ergebnis bleibt sofort sichtbar ohne Gate, aber Versand ist freiwilliger Zusatznutzen), ohne das „ohne Anmeldung"-Versprechen zu brechen.
- **Eigene Daten einfließen lassen**: anonymisierte Erfahrungswerte aus Risikovoranfragen/Beratungen (typische Beitragsspannen nach Alter, Dienstherr) als Vergleichswert neben der reinen Modellrechnung – genau der „Erfahrung statt Recherche"-Hebel aus der Ressourcen-Notiz, den kein Wettbewerber kopieren kann.

### 3. Handlungsaufforderungen für den Nutzer

Nach dem Vorbild des Konkurrenten (Ergebnis zuerst, dann Beratung anbieten), aber mit stärkerer Verzahnung zum eigenen USP:

- Primärer CTA direkt am Ergebnis: „Kostenloses Beratungsgespräch zu deiner Versorgungslücke" (nicht generisch „Termin buchen", sondern an das konkrete Rechenergebnis angebunden).
- Sekundärer, niedrigschwelliger CTA: Ergebnis per PDF/E-Mail sichern – das ist der legitime Lead-Erfassungspunkt, ohne das Ergebnis selbst zu gaten.
- Tertiär: passender Ratgeberartikel verlinkt, je nach Ergebnis-Schwerpunkt (z. B. hohe Pensionslücke → Link zu Altersvorsorge-Inhalten; PKV-Beitrag im Fokus → Link zu PKV-Ratgebern). Damit wird der Rechner zum internen Linkhub statt Sackgasse.

### 4. Risiken/offene Punkte

- **Entwicklungsaufwand**: Ein funktionierender Rechner ist technischer Aufbau, kein Content-Task – Klärung mit Sven, wer das umsetzt (WordPress-Plugin, Custom-Entwicklung, No-Code-Tool).
- **Pflegeaufwand**: Besoldungstabellen ändern sich jährlich/bundeslandweise. Ohne laufende Aktualisierung verliert der Rechner schnell an Vertrauen und Ranking – Prozess dafür muss von Anfang an mitgedacht werden (vgl. Vault-Regel zu wiederkehrenden Messwerten bei anderen fairbeamtet-Dateien).
- **Rechtlich/fachlich**: Berechnungslogik (Besoldung, Beihilfe, PKV-Modellrechnung) muss faktengeprüft sein, YMYL-Thema. Bei Umsetzung early mit Sven/fachlicher Prüfung abstimmen, nicht nur mit SEO-Brille bauen.
- **Daten für eigene Werte**: Welche eigenen Daten (Risikovoranfragen, Beitragsspannen) tatsächlich auswertbar und nutzbar sind, ist laut [[04 Ressourcen/Googles No. 1/Originaere Daten Tools und Experience.md|Originäre Daten, Tools und Experience]] noch offen und eine Frage an PW – vor Umsetzung klären.

## Nächste Schritte

- [ ] Mit Sven abstimmen: Prioität und Umsetzungsweg (intern entwickeln vs. Agentur/Tool) für einen eigenen Rechner klären
- [ ] Entscheiden: Reiner Gehalts-/Besoldungsrechner vs. breiterer Beihilfe-/PKV-/Vorsorge-Lückenrechner (Empfehlung: Letzteres, näher am eigenen Angebot)
- [ ] Klären, welche eigenen Daten (Risikovoranfragen, Beitragsspannen) für den Rechner nutzbar sind
- [ ] Entwurf CTA- und Lead-Logik (PDF-Export, Beratungstermin-Anbindung) mit Sven abstimmen
- [ ] Pflegeprozess für jährliche Besoldungstabellen-Updates definieren, bevor der Rechner live geht
- [ ] Traffic-Entwicklung der neuen einfachverbeamtet-Artikel (DU, PKV, Diensthaftpflicht, seit 08.11.2026) weiter beobachten – siehe „Ausblick" im Wettbewerber-Steckbrief
