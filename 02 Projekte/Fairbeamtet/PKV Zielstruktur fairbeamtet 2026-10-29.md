---
tags:
  - seo
  - fairbeamtet
date: 2026-10-29
---

# PKV Zielstruktur fairbeamtet.de

> [!info] Export aus Svens Vault, Stand 29.10.2026
> Das ist eine Kopie. Das Original steht in Svens Vault unter „04 Ressourcen/PKV Keyword-Map/PKV Zielstruktur" und wird dort weitergepflegt. Bei Widersprüchen gilt das Original. Begriffe wie Claudia, Seitenauftrag oder Arbeitshandbuch beziehen sich auf Svens Ablauf für die Ratgeber-Texte.

Die optimale Struktur und Hierarchie der PKV-Seiten auf fairbeamtet.de. Fassung 3 vom 29.10.2026: Zielgruppen bekommen Kind-Seiten je Thema. Fassung 2, von Sven festgelegt am 24.10.2026, ersetzte die Struktur der ersten Fassung mit 442 Seiten aus PKV Keyword-Map. Gilt nur für die PKV, Beihilfe und BU/DU bekommen eigene Strukturen.


## Regeln

Grundlage: Search Intent und Haupt-Hub, Topical Authority ohne Kannibalisierung, Interne Verlinkung und Informationsarchitektur.

1. **Fokus: PKV für Beamte.** Seiten mit Relevanz „rand" sind gestrichen (105): andere Zielgruppen, Unterseiten zu Zusatzversicherungen, Service der Versicherer. Zusatzversicherung, Krankentagegeld und Abrechnung bleiben als je eine Seite für Beamte.
2. **Eine Frage, eine Seite.** Zielgruppen-Varianten wie `/pkv/kosten/beamte/` werden Abschnitt der Elternseite (66), weil die ganze Website für Beamte spricht. `/pkv/beamte/` geht in `/pkv/` auf. **Ausnahme seit 29.10.2026 (Fassung 3):** Hat die Zielgruppe eine eigene Seite (Lehrer, Referendare, Beamtenanwärter, Pensionäre, Polizei), bekommt jede ihrer Themen-Varianten eine eigene **Kind-Seite unter der Zielgruppe**: `/pkv/lehrer/kosten/`, nicht `/pkv/kosten/lehrer/`. Die Zielgruppen-Seite wird damit Eltern-Seite. Die Themen-Seite (`/pkv/kosten/`) und die Zielgruppen-Kind-Seite verweisen gegenseitig mit Teasern aufeinander. Die Zielgruppen-Kind-Seite erklärt nur, was für diese Zielgruppe anders ist, und verlinkt für die Grundlagen die Themen-Seite. Varianten für „Beamte" bleiben Abschnitte der Themen-Seiten, weil die ganze Website für Beamte spricht. Varianten von Anbietern (Debeka ❯ Beamtenanwärter) bleiben auf der Anbieter-Seite. Grund: Messung und Entscheidung vom 29.10.2026, siehe unten.
3. **Vergleich gebündelt.** „Beste PKV" und „Test" sind Abschnitte von `/pkv/vergleich/`. Anlass: Messung vom 30.09.2026, acht eigene URLs für „beste private krankenversicherung beamte", keine in den Top 10.
4. **Eine starke Seite je Anbieter.** Unterseiten bekommt ein Anbieter nach Regel 9, nicht nach Suchvolumen. Die Schwelle von 300 Suchen ist am 29.10.2026 gestrichen (Sven). Die 183 Anbieter-Abschnitte werden beim Bau der jeweiligen Anbieter-Seite einzeln geprüft. Die Beitragserhöhung eines Anbieters steht als Abschnitt auf der Anbieter-Seite und verlinkt das Jahresarchiv.
5. **Höchstens drei Ebenen:** `/pkv/` ❯ Thema ❯ Unterthema. Ausnahme ist das Jahresarchiv `/pkv/beitragserhoehung/JJJJ/anbieter/`.
6. **Navigation:** 7 Menüpunkte und ein Button „Beratung". Das Menü ist keine URL-Ebene.
7. **Kategorien erst ab mehreren Beiträgen.** Weniger als drei Beiträge zu einem Thema sind Einzel-Beiträge ohne eigene Kategorie.
8. **Höchstens drei Klicks.** Jede Seite ist von jeder anderen Seite aus mit höchstens drei Klicks erreichbar, jeder Abschnitt einer Seite auch. Von Sven festgelegt am 29.10.2026, nach Steve Jobs. Erfüllt wird das so: Das Menü steht auf jeder Seite und erreicht alle Seiten der zweiten Ebene mit einem Klick. Seiten der dritten Ebene sind zwei Klicks entfernt, Anbieter-Unterseiten und das Jahresarchiv drei (Menü ❯ Anbieter ❯ Debeka ❯ Kosten). Jede Seite mit mehr als drei H2 hat ein Inhaltsverzeichnis mit Sprungmarken, damit auch ein Abschnitt innerhalb des Limits bleibt. Eine vierte Ebene würde die Regel brechen.
9. **Seite oder Abschnitt entscheidet der Leser, nicht das Suchvolumen.** Von Sven festgelegt am 29.10.2026. Suchvolumen spielt keine Rolle. Auch Suchanfragen ohne gemessenes Volumen bringen Besucher, etwa Anfragen aus der Search Console, Fragen aus Foren und aus der Beratung. Ziel ist, jedes Keyword sauber unterzubringen und das Thema vollständig abzudecken, egal ob über Eltern- und Kind-Seiten oder über Kategorien und Beiträge.
   - **Eigene Seite**, wenn beides zutrifft: Es ist eine eigene Frage (Overlap-Score unter 40 % oder für den Leser erkennbar eine andere Frage), **und** die Antwort würde die Eltern-Seite schwerer benutzbar machen. Das ist zum Beispiel der Fall, wenn der Abschnitt eigene H3 braucht oder mehr als etwa ein Drittel der Seite einnehmen würde. Das Drittel ist ein gesetzter Wert.
   - **Abschnitt**, wenn es dieselbe Frage ist wie auf der Eltern-Seite (Beamten-Varianten nach Regel 2, „Beste" und „Test" nach Regel 3) oder wenn die Antwort in wenige Sätze passt.
   - **Die Länge ist ein Kriterium für die Lesbarkeit und kein Ziel für das Ranking.** Eine Seite ist so lang, wie ihre Frage es braucht. Google kennt keine Mindestlänge (Search Intent und Haupt-Hub). Wird eine Seite so lang, dass der Leser seine Antwort nicht schnell findet, wird geteilt.
   - Entschieden wird beim Bau von oben nach unten: Claudia legt beim Bau der Eltern-Seite in Schritt 3 für jeden Abschnitt einen Vorschlag vor, Sven entscheidet.

Die Grenze in Regel 5 ist gesetzt, keine Google-Vorgabe. Vor dem Bau der großen Zusammenlegungen (Kosten, Vergleich, Debeka) mit dem Overlap-Score prüfen, ob es wirklich eine Suchabsicht ist.

## Seitentypen und Bau-Reihenfolge

Von Sven festgelegt am 29.10.2026. Jede Seite hat einen von drei Typen, und der Typ bestimmt den Umfang des Textes. Claudia ermittelt ihn mit `seitenauftrag.py`, Ablauf im Arbeitshandbuch, Schritt 2.

| Typ | Seiten | Umfang |
|---|--:|---|
| **A · Eltern-Seite** (hat Kind-Seiten) | 24 | Hauptfrage vollständig, je Kind-Seite ein Teaser mit Kernantwort und Link |
| **B · Kind-Seite** (Eltern-Seite ist nicht `/pkv/`) | 49 | ein Thema in die Tiefe, Link nach oben |
| **C · Einzelseite** (direkt unter `/pkv/`) | 49 | Thema vollständig |

Ein Thema mit eigener Seite steht überall sonst nur als Teaser. Auf `/pkv/` gibt es einen Teaser je Menügruppe, nicht je Kind-Seite.

**Gebaut wird von oben nach unten:** erst die Eltern-Seiten, dann deren Kind-Seiten, Ebene für Ebene, bis das Thema vollständig abgearbeitet ist. `status` in der Seiten-Notiz zeigt, was steht: `geplant`, `entwurf`, `veröffentlicht`.

## Navigation

- **Button:** Beratung `/pkv/beratung/`
- **Einstieg**
  - PKV für Beamte `/pkv/`
  - Voraussetzungen `/pkv/voraussetzungen/`
  - PKV oder GKV `/pkv/pkv-oder-gkv/`
  - Anwartschaft und Optionstarif `/pkv/anwartschaft/`
- **Für wen**
  - Beamtenanwärter `/pkv/beamtenanwaerter/`
  - Referendare `/pkv/referendare/`
  - Lehrer `/pkv/lehrer/`
  - Polizei `/pkv/polizei/`
  - Pensionäre `/pkv/pensionaere/`
  - Familie und Kinder `/pkv/familie/`
- **Kosten**
  - Kosten `/pkv/kosten/`
  - Beitragserhöhung `/pkv/beitragserhoehung/`
  - Beitragsrückerstattung `/pkv/beitragsrueckerstattung/`
- **Vergleich und Anbieter**
  - Vergleich und Test `/pkv/vergleich/`
  - Anbieter `/pkv/anbieter/`
  - Erfahrungen `/pkv/erfahrungen/`
- **Gesundheitsprüfung**
  - Gesundheitsprüfung und Vorerkrankungen `/pkv/gesundheitspruefung/`
  - Öffnungsaktion `/pkv/oeffnungsaktion/`
- **Leistungen und Tarife**
  - Leistungen `/pkv/leistungen/`
  - Tarife `/pkv/tarife/`
  - Pflegepflichtversicherung `/pkv/pflegepflichtversicherung/`
  - Zusatzversicherung `/pkv/zusatzversicherung/`
  - Krankentagegeld `/pkv/krankentagegeld/`
  - Ausland `/pkv/ausland/`
  - Abrechnung und Service `/pkv/service/`
- **Wechsel und Alter**
  - Wechsel `/pkv/wechsel/`
  - Tarifwechsel `/pkv/tarifwechsel/`
  - Basistarif und Sozialtarife `/pkv/basistarif/`
  - PKV im Alter `/pkv/alter/`

## Messung 29.10.2026: Zielgruppe und Thema

Frage: Bekommen Zielgruppen eigene Kind-Seiten wie `/pkv/lehrer/kosten/`? Gemessen mit dem SERP Overlap Score (Search Intent und Haupt-Hub), Ahrefs SERP-Übersicht, Deutschland, organische Top 10. Ahrefs liefert je Anfrage 8 bis 9 organische URLs, Stand der Ergebnisse 26.09. bis 26.10.2026.

| Anfrage | gegen Themen-Anfrage | gegen Zielgruppen-Anfrage | Wer rankt |
|---|--:|--:|---|
| lehrer private krankenversicherung kosten | 0 % (private krankenversicherung kosten) | 0 % (private krankenversicherung lehrer) | 5 von 8 Lehrer-Seiten, 3 Kosten-Seiten |
| private krankenversicherung referendariat lehramt kosten | 0 % (private krankenversicherung kosten) | 0 % (private krankenversicherung referendariat) | 9 von 9 Referendariats-Seiten, keine Kosten-Seite |
| freie heilfürsorge gesetzlich oder privat | 0 % (gesetzliche private krankenversicherung) | keine Daten | überwiegend Seiten für Polizeibeamte |
| krankenversicherung beamte kosten | 0 % (private krankenversicherung kosten) | 0 % (private krankenversicherung beamte) | Kosten-Seiten für Beamte |
| beste private krankenversicherung beamte | 0 % (pkv vergleich) | 20 % (private krankenversicherung beamte) | Vergleichsseiten für Beamte |

Für „pkv vergleich beamtenanwärter", „beste pkv für beamtenanwärter", „pkv lehrer vergleich", „private krankenversicherung vergleich referendariat", „private krankenversicherung pension kosten" und „krankenversicherung für polizisten" hat Ahrefs keine SERP gespeichert. Die Daten zu „krankenversicherung für pensionäre" sind von 2024 und wurden nicht verwendet.

**Befund:**
1. Zielgruppe und Thema zusammen sind eine eigene Suchabsicht. Google beantwortet sie vor allem mit **Zielgruppen-Seiten**, nicht mit Themen-Seiten. Deshalb hängen die Varianten unter der Zielgruppe (Regel 2, Ausnahme).
2. **Das Volumen ist klein:** 50 bis 270 Suchen im Monat je Kombination, zusammen 960. **Sven hat am 29.10.2026 trotzdem eigene Seiten festgelegt:** Wer „PKV Kosten Lehrer" sucht, soll genau diese Antwort schnell finden und sich nicht durch eine lange Seite lesen müssen. Lieber fünf Seiten mit je 50 zufriedenen Suchenden als eine mit 250 unzufriedenen. Voraussetzung ist eine saubere Trennung der Keywords, damit sich die Seiten nicht gegenseitig Konkurrenz machen. Die Drei-Klick-Regel bleibt erfüllt (Menü ❯ Lehrer ❯ Kosten).
3. Gemessen sind Lehrer, Referendare und Polizei. Für Beamtenanwärter und Pensionäre gilt dieselbe Regel, weil sie für den Leser logisch ist. Gemessen ist sie dort nicht. „Beste PKV für Beamtenanwärter" ist nach Regel 3 Abschnitt von `/pkv/beamtenanwaerter/vergleich/`.
4. **Allgemeine Anfragen und Anfragen von Beamten überschneiden sich nicht** (0 % bei Kosten und bei Vergleich). Bei „private krankenversicherung kosten" und „pkv vergleich" ranken Check24, Allianz und Finanztip für alle Zielgruppen. Siehe „Offen".

Die Werte stammen aus einer Stichprobe und sind kein Nachweis. Bei niedrigem Volumen sind identische URLs selten, ein Teil der 0 % kann daher Zufall sein. Eindeutig ist dagegen, welche Art von Seite rankt.

## 1 · Seiten mit Eltern/Kind-Struktur

19 Eltern-Seiten, 72 Seiten.

### Themen

- Kosten `/pkv/kosten/`
  - Beitragsrechner `/pkv/kosten/beitragsrechner/`
  - Günstige PKV `/pkv/kosten/guenstige-pkv/`
  - Arbeitgeberzuschuss `/pkv/kosten/arbeitgeberzuschuss/`
  - Höchstbeitrag `/pkv/kosten/hoechstbeitrag/`
  - Selbstbeteiligung `/pkv/kosten/selbstbeteiligung/`
  - Steuer `/pkv/kosten/steuer/`
- Vergleich und Test `/pkv/vergleich/`
  - Vergleichsrechner `/pkv/vergleich/vergleichsrechner/`
  - DKV oder ERGO `/pkv/vergleich/dkv-oder-ergo/`
  - DBV oder Debeka `/pkv/vergleich/dbv-oder-debeka/`
  - Debeka oder HUK-Coburg `/pkv/vergleich/debeka-oder-huk-coburg/`
  - Die Bayerische oder Versicherungskammer Bayern `/pkv/vergleich/die-bayerische-oder-versicherungskammer-bayern/`
- Wechsel `/pkv/wechsel/`
  - Zurück in die GKV `/pkv/wechsel/zurueck-in-die-gkv/`
  - Wechsel von GKV in PKV `/pkv/wechsel/gkv-zu-pkv/`
  - Kündigung `/pkv/wechsel/kuendigung/`
- Basistarif und Sozialtarife `/pkv/basistarif/`
  - Standardtarif `/pkv/basistarif/standardtarif/`
  - Notlagentarif `/pkv/basistarif/notlagentarif/`
- PKV im Alter `/pkv/alter/`
  - Altersrückstellungen `/pkv/alter/altersrueckstellungen/`
  - PKV ab 55 `/pkv/alter/ab-55/`
  - Beitragsentlastung `/pkv/alter/beitragsentlastung/`
- Gesundheitsprüfung und Vorerkrankungen `/pkv/gesundheitspruefung/`
  - Psychotherapie und psychische Erkrankungen `/pkv/gesundheitspruefung/psychotherapie/`
  - Risikozuschlag `/pkv/gesundheitspruefung/risikozuschlag/`
- Familie und Kinder `/pkv/familie/`
  - Ehepartner `/pkv/familie/ehepartner/`
  - Kinder `/pkv/familie/kinder/`
  - Schwangerschaft und Elternzeit `/pkv/familie/schwangerschaft-elternzeit/`
- Beitragserhöhung `/pkv/beitragserhoehung/`
  - Beitragsentwicklung `/pkv/beitragserhoehung/beitragsentwicklung/`
  - Unwirksame Beitragserhöhung `/pkv/beitragserhoehung/unwirksame-beitragserhoehung/`
  - 2020 `/pkv/beitragserhoehung/2020/`
    - Barmenia `/pkv/beitragserhoehung/2020/barmenia/`
    - Concordia `/pkv/beitragserhoehung/2020/concordia/`
  - 2021 `/pkv/beitragserhoehung/2021/`
    - Debeka `/pkv/beitragserhoehung/2021/debeka/`
  - 2025 `/pkv/beitragserhoehung/2025/`
    - Debeka `/pkv/beitragserhoehung/2025/debeka/`
  - 2027 `/pkv/beitragserhoehung/2027/`
    - Debeka `/pkv/beitragserhoehung/2027/debeka/`
- Leistungen `/pkv/leistungen/`
  - Krankenhaus `/pkv/leistungen/krankenhaus/`
  - Zahnleistungen `/pkv/leistungen/zahnleistungen/`
  - Privatpatient `/pkv/leistungen/privatpatient/`
- Tarifwechsel `/pkv/tarifwechsel/`
  - Beitrag senken `/pkv/tarifwechsel/beitrag-senken/`
  - Unisex und Bisex `/pkv/tarifwechsel/unisex-bisex/`

### Zielgruppen

- Beamtenanwärter `/pkv/beamtenanwaerter/`
  - Vergleich `/pkv/beamtenanwaerter/vergleich/`
- Referendare `/pkv/referendare/`
  - Kosten `/pkv/referendare/kosten/`
  - Vergleich `/pkv/referendare/vergleich/`
- Lehrer `/pkv/lehrer/`
  - Kosten `/pkv/lehrer/kosten/`
  - Vergleich `/pkv/lehrer/vergleich/`
- Pensionäre `/pkv/pensionaere/`
  - Kosten `/pkv/pensionaere/kosten/`
- Polizei `/pkv/polizei/`
  - PKV oder GKV `/pkv/polizei/pkv-oder-gkv/`

### Anbieter

- Debeka PKV `/pkv/debeka/`
  - Kosten `/pkv/debeka/kosten/`
  - Tarifwechsel `/pkv/debeka/tarifwechsel/`
  - Öffnungsaktion `/pkv/debeka/oeffnungsaktion/`
- Barmenia PKV `/pkv/barmenia/`
  - Erfahrungen `/pkv/barmenia/erfahrungen/`
- Allianz PKV `/pkv/allianz/`
  - Kosten `/pkv/allianz/kosten/`
- HUK-Coburg PKV `/pkv/huk-coburg/`
  - Erfahrungen `/pkv/huk-coburg/erfahrungen/`

## 2 · Kategorien und Beiträge

Keine. „PKV aktuell" entsteht erst, wenn mehrere datierte Anlässe zusammenkommen. Keine Unterkategorien.

## 3 · Einzel-Seiten

48 Seiten ohne Kind-Seiten, direkt unter `/pkv/`.

### Themen

- Zusatzversicherung `/pkv/zusatzversicherung/`
- Voraussetzungen `/pkv/voraussetzungen/`
- PKV oder GKV `/pkv/pkv-oder-gkv/`
- Abschluss und Beratung `/pkv/beratung/`
- Pflegepflichtversicherung `/pkv/pflegepflichtversicherung/`
- Anwartschaft und Optionstarif `/pkv/anwartschaft/`
- Krankentagegeld `/pkv/krankentagegeld/`
- Öffnungsaktion `/pkv/oeffnungsaktion/`
- Abrechnung und Service `/pkv/service/`
- Tarife `/pkv/tarife/`
- Ausland `/pkv/ausland/`
- Beitragsrückerstattung `/pkv/beitragsrueckerstattung/`
- Erfahrungen `/pkv/erfahrungen/`

### Anbieter

- Anbieter `/pkv/anbieter/`
- DKV PKV `/pkv/dkv/`
- DBV PKV `/pkv/dbv/`
- HanseMerkur PKV `/pkv/hansemerkur/`
- AXA PKV `/pkv/axa/`
- Signal Iduna PKV `/pkv/signal-iduna/`
- Hallesche PKV `/pkv/hallesche/`
- ARAG PKV `/pkv/arag/`
- DEVK PKV `/pkv/devk/`
- Continentale PKV `/pkv/continentale/`
- UKV PKV `/pkv/union-krankenversicherung/`
- Universa PKV `/pkv/universa/`
- Generali PKV `/pkv/generali/`
- LKH PKV `/pkv/lkh/`
- LVM PKV `/pkv/lvm/`
- Postbeamtenkrankenkasse PKV `/pkv/postbeamtenkrankenkasse/`
- ERGO PKV `/pkv/ergo/`
- Gothaer PKV `/pkv/gothaer/`
- SDK PKV `/pkv/sdk/`
- KVB PKV `/pkv/kvb/`
- INTER PKV `/pkv/inter/`
- ottonova PKV `/pkv/ottonova/`
- Alte Oldenburger PKV `/pkv/alte-oldenburger/`
- vigo PKV `/pkv/vigo/`
- Central PKV `/pkv/central/`
- Concordia PKV `/pkv/concordia/`
- Bayerische Beamtenkrankenkasse PKV `/pkv/bayerische-beamtenkrankenkasse/`
- Nürnberger PKV `/pkv/nuernberger/`
- Versicherungskammer Bayern PKV `/pkv/versicherungskammer-bayern/`
- Pax-Familienfürsorge PKV `/pkv/pax/`
- Provinzial PKV `/pkv/provinzial/`
- Münchener Verein PKV `/pkv/muenchener-verein/`
- Envivas PKV `/pkv/envivas/`
- Württembergische PKV `/pkv/wuerttembergische/`
- R+V PKV `/pkv/r-v/`

## 4 · Einzel-Beiträge

- Zukunft der PKV `/pkv-zukunft/`

## Offen

Alle Punkte werden geprüft, wenn Claudia die Debeka-Seiten und -Beiträge erstellt (Sven am 24.10.2026). Sie legt sie in Schritt 3 vor, Sven entscheidet, danach wird der Punkt hier gestrichen. Verankert im Arbeitshandbuch, Schritt 2.

- Overlap-Score für Kosten, Vergleich und Debeka vor dem Bau prüfen.
- `/jahresarbeitsentgeltgrenze/` zielte auf die gestrichene Seite PKV ❯ Voraussetzungen ❯ Angestellte und hat in der Zielstruktur keinen Platz.
- **Hauptkeyword von Kosten und Vergleich:** `private krankenversicherung kosten` (12.100) und `pkv vergleich` werden laut Messung vom 29.10.2026 für alle Zielgruppen ausgespielt und überschneiden sich zu 0 % mit den Anfragen von Beamten. Beim Bau der beiden Seiten prüft Claudia in Schritt 3, ob das Fokus-Keyword die Beamten-Variante sein soll (`krankenversicherung beamte kosten`, `beste private krankenversicherung beamte`). Sven entscheidet.
- Mehrere bestehende Beiträge zielen jetzt auf dieselbe Seite, etwa drei auf `/pkv/vergleich/`. Der Befund in den Bestand-Notizen steht noch auf „passt" und wird beim Bau auf „zusammenlegen" gesetzt.