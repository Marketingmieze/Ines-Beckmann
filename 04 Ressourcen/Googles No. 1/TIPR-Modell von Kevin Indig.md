---
tags:
  - ressource
  - seo
date: 2026-09-27
---

# TIPR-Modell von Kevin Indig

Vertiefung zu [[Interne Verlinkung und Informationsarchitektur]]. Das bekannteste systematische Modell, um interne Verlinkung nicht nach Gefühl, sondern nach Zahlen zu steuern.

**Vorweg das Urteil:** Kevins Vollmodell ist für fairbeamtet.de zu schwer — er selbst grenzt es auf mittelgroße bis große Websites ein. Die vereinfachte Fassung von Alexander Außermayr dagegen ist machbar, sobald Screaming Frog und ein Ahrefs-Zugang da sind. Sie ersetzt die PageRank-Rechnung durch eine Subtraktion.

## Was TIPR ist

**TIPR = True Internal PageRank.** Vorgestellt von Kevin Indig 2018 auf der Tech SEO Boost in Boston, ausführlicher Beitrag vom 04.12.2018, vereinfachte Fassung „TIPR lite" vom 21.03.2022.

Sein Ausgangsärger, wörtlich:

> „Internal link graphs exist in isolation and don't factor in backlinks. That's why I came up with the TIPR model."

Und auf einer Folie seines Vortrags:

> „Internal PageRank is only half of the equation."

Der Punkt: Wer nur zählt, wie oft eine Seite intern verlinkt ist, übersieht, dass manche Seiten ihre Stärke von außen beziehen. Eine Seite mit vielen Backlinks ist stark, auch wenn intern kaum etwas auf sie zeigt — und sie sollte diese Stärke weitergeben.

## Die vier Zutaten

| Kennzahl | Was sie misst |
|---|---|
| **Internal PageRank** | Linkkraft, die eine Seite über interne **eingehende** Links **erhält** |
| **CheiRank** | Umgekehrter PageRank: Linkkraft, die eine Seite über interne **ausgehende** Links **abgibt** |
| **Backlinks** | Autorität, die von außen auf die Seite trifft |
| **Logfiles** | Wie oft der Googlebot die Seite tatsächlich crawlt |

CheiRank ist der Begriff, der die meisten stolpern lässt. Indigs Formulierung:

> „PageRank is the link power received, but CheiRank is the link power that is given away."

Und der Zweck der Gegenüberstellung:

> „CheiRank helps to measure whether pages with high PR give away enough to other pages, while PageRank helps you measure whether important pages have enough PageRank."

## Waster und Hoarder

Das Ziel des Modells ist, zwei Fehlertypen zu finden:

**Hoarder — der Hamsterer.** Eine Seite mit hohem PageRank und niedrigem CheiRank. Sie bekommt viel Linkkraft und gibt kaum etwas weiter. Typisch: eine starke Ratgeberseite, die auf nichts verlinkt. Die Stärke versickert dort.

**Waster — der Verschwender.** Eine Seite, die ihre Linkkraft an Ziele abgibt, die sie nicht brauchen. Typisch: ein Footer, der auf Impressum, Datenschutz und AGB verlinkt, während die Geldseiten kaum interne Links bekommen.

Beides sind Ungleichgewichte zwischen dem, was hereinkommt, und dem, was hinausgeht.

## Das Robin-Hood-Prinzip

Indigs Leitsatz zur Korrektur:

> „Take from the rich, give to the poor."

Linkkraft von überversorgten Seiten zu den Seiten umleiten, die tatsächlich Umsatz bringen. Der Hintergedanke: Interne Verlinkung folgt fast immer einer Potenzverteilung — wenige Seiten sammeln tausende Links, die große Mehrheit bekommt eine Handvoll. Das Modell soll diese Kurve abflachen.

## Die sechs Schritte

1. Website crawlen
2. Internen PageRank und CheiRank berechnen
3. Backlinkdaten ergänzen — daraus wird der „echte" interne PageRank
4. Crawl-Häufigkeit aus den Logfiles ergänzen
5. Kennzahlen sortieren und in eine Rangfolge bringen
6. Die umsatzrelevanten Seiten optimieren

## Wie die Rangfolge gebildet wird

Das ist der praktisch wichtigste Teil und überraschend simpel. **Jede Kennzahl wird für sich sortiert und bekommt einen Rang. Dann wird der Mittelwert der Ränge gebildet und danach neu sortiert.**

| URL | Crawl-Frequenz | Domain Popularity | PageRank | CheiRank | Ø-Rang |
|---|---:|---:|---:|---:|---:|
| /URL1 | 2 | 1 | 1 | 1 | 1,25 |
| /URL3 | 1 | 3 | 2 | 3 | 2,25 |

Keine gewichtete Formel, kein Score. Nur vier Ranglisten und ihr Durchschnitt. Das Ergebnis ist eine Prioritätenliste: Welche Seiten stehen im Verhältnis zu ihrer Bedeutung schlecht da?

## TIPR lite — die abgespeckte Fassung

Die Vollfassung braucht Logfile-Analyse, und die haben die wenigsten. Deshalb die Lite-Variante von 2022. Dafür reichen **drei Dinge**:

1. **Google Sheets, Excel oder LibreOffice Calc**
2. **Ahrefs** mit API-Zugang (Backlinkdaten)
3. **Screaming Frog SEO Spider** oder ein anderer Crawler

Die Logfiles fallen weg, damit auch die Crawl-Frequenz.

## Die praktikabelste Umsetzung: Alexander Außermayr

Kevins eigene TIPR-Beiträge stehen hinter einer Paywall. Die beste frei zugängliche Anleitung stammt von **Alexander Außermayr**, selbstständiger SEO-Consultant aus Salzburg: [Kevin Indigs „TIPR Lite" noch leichter](https://aussermayr.com/blog/tipr-lite-interne-verlinkung), Stand 17.09.2022.

Er vereinfacht die Lite-Fassung weiter, indem er die Datensammlung über die **Ahrefs-API direkt in Screaming Frog** automatisiert. Seine Begründung, angenehm unprätentiös:

> „Effizientes operatives Arbeiten ist in meinem Alltag als selbstständiger SEO Consultant äußerst wichtig."

### Der entscheidende Kniff: Delta statt PageRank

Statt echten PageRank und CheiRank zu berechnen, nimmt er die Zahlen, die Screaming Frog ohnehin liefert:

```
Delta = Inlinks − Outlinks
```

**Das ist der operative Kern.** Inlinks stehen für empfangene Linkkraft, Outlinks für abgegebene — die Differenz zeigt das Ungleichgewicht. Keine Matrixrechnung, keine Iteration, eine Subtraktion in einer Tabellenspalte.

### Schritt für Schritt

**1. Screaming Frog konfigurieren**
Unter `Configuration > Spider` auf interne HTML-Seiten beschränken. Vorher klären: Braucht die Seite JavaScript-Rendering? Gibt es Login-Bereiche oder eine Staging-Umgebung?

**2. Ahrefs anbinden**
`Configuration > API Access > Ahrefs`. Im Reiter *Account Information* den API Access Token eintragen, **Connect**, auf den grünen **Connected**-Banner warten. Ohne Token: über *generate an API access token* einen erzeugen und Screaming Frog den Zugriff erlauben.

**3. Genau zwei Metriken aktivieren**
Im Reiter *Metrics*, Gruppe **URL (Exact Match)**, nur diese zwei:
- **Backlinks**
- **RefDomains**

Außermayr warnt ausdrücklich davor, mehr zu nehmen. URL Rating, Keywords, Link Score, External Outlinks, JS Outlinks — alles möglich, alles macht die Aufbereitung unnötig kompliziert.

**4. Crawlen**
Vollständig durchlaufen lassen. Bei hoher Crawl-Geschwindigkeit hängt die Ahrefs-API ein paar Sekunden nach. Fertig ist es, wenn oben rechts **drei grüne Balken** stehen.

**5. Exportieren**
Reiter **Internal** öffnen, das Dropdown links oben auf **HTML** stellen, **Export** als CSV.

**6. Bereinigen**
- Alle Zeilen mit **Statuscode ≠ 200** löschen
- Alle nicht linkbezogenen Spalten entfernen
- Neue Spalte **`Delta`** anlegen: `Inlinks − Outlinks`
- Spalten umbenennen: *„Ahrefs Backlinks - Exact"* → `Backlinks`, *„Ahrefs RefDomains - Exact"* → `RefDomains`

Übrig bleiben sechs Spalten:

| URL | Inlinks | Outlinks | Delta | Backlinks | RefDomains |
|---|---|---|---|---|---|

Gemeint sind die **Unique** Inlinks und Outlinks, nicht die Gesamtzahl.

**7. Auswerten**
Nach `Delta` sortieren, dann gegen `Backlinks` und `RefDomains` halten. Kevin Indigs eigene Formulierung dessen, was man sucht:

> „looking for two things: 1) pages with a lot of incoming links that don't link out much and 2) pages with few incoming links that do link out a lot"

| Muster | Delta | Befund | Maßnahme |
|---|---|---|---|
| Viele Inlinks, wenige Outlinks, dazu Backlinks | stark positiv | **Autoritäts-Horter** | Ausgehende interne Links setzen, Linkkraft weiterreichen |
| Wenige Inlinks, viele Outlinks | stark negativ | **Verschwender oder Waise** | Eingehende Links besorgen — oder ausgehende reduzieren |

Beim zweiten Typ ist die Quelle nicht eindeutig: Außermayr denkt eher ans Entfernen ausgehender Links, die gängigere Lesart ist, eingehende hinzuzufügen. **Beides ist vertretbar, die Entscheidung hängt daran, ob die Seite selbst wichtig ist.** Ist sie wichtig, gehören Inlinks her. Ist sie es nicht, verschwendet sie Kraft und sollte weniger streuen.

### Was bewusst fehlt

Außermayr lässt die **Incoming Link Position** weg — also die Unterscheidung, ob ein Link aus der Navigation, dem Inhalt oder dem Footer kommt. Begründung: Sie verkompliziert die Aufbereitung. Für eine gründliche Analyse ist das ein echter Verlust, denn ein Link aus dem Fließtext wiegt anders als einer aus dem Footer. Für eine schnelle Bestandsaufnahme ist der Verzicht vertretbar.

**Schwellenwerte nennt keine der Quellen.** Es gibt kein „ab Delta 20 handeln". Man sortiert, schaut sich die Extreme an und entscheidet je Seite.

## Kevins eigene Einschränkungen

Das rechne ich ihm hoch an, er nennt sie auf seinen eigenen Folien:

- TIPR ist **nur ein Rankingfaktor unter vielen**
- Geeignet **nur für mittelgroße bis große Websites**
- Die **Gewichtung der Faktoren ist nicht sauber kalibriert**
- Bisher **nur auf wenigen Websites getestet**

Das ist deutlich mehr Zurückhaltung, als die meisten SEO-Modelle mitbringen.

## Taugt das für fairbeamtet.de?

**Kevins Vollmodell: nein.** Es lebt davon, in hunderten oder tausenden URLs Muster zu finden, die man von Hand nicht mehr sieht, und braucht Logfile-Zugriff. Er selbst grenzt den Anwendungsbereich auf mittelgroße bis große Websites ein.

**Außermayrs Delta-Variante: ja, sobald die Werkzeuge da sind.** Der Aufwand ist ein Crawl, ein Export und eine Tabellenspalte. Das lohnt auch bei fünfzig Seiten, weil man hinterher schwarz auf weiß sieht, welche Seite hortet und welche verhungert — statt es zu schätzen.

**Was es dafür braucht:**

| Werkzeug | Kosten | Ersatz möglich? |
|---|---|---|
| Screaming Frog SEO Spider | bis 500 URLs kostenlos, darüber kostenpflichtig | Ja, jeder Crawler, der Unique Inlinks und Outlinks exportiert |
| Ahrefs mit API-Zugang | kostenpflichtig | Schwer zu ersetzen. Ohne Backlinkdaten bleibt Delta allein — immer noch nützlich, aber ohne die externe Hälfte |

**Das ist geklärt.** Die Sitemap von fairbeamtet.de führt am 27.09.2026 **283 URLs** (218 Beiträge, 34 Seiten, 21 Kategorien, 4 Autoren, 5 Videos, 1 Local), die Search Console kennt 278. **Unter 500 — die kostenlose Screaming-Frog-Fassung reicht für den Crawl.** Und Ahrefs ist über Svens Zugang ebenfalls da. Beide Voraussetzungen sind erfüllt, die Analyse kann laufen, sobald die zehn Hebel stehen. Und selbst ohne Ahrefs ist die Delta-Spalte schon der halbe Nutzen — genau das Ungleichgewicht zwischen eingehenden und ausgehenden internen Links, das man sonst nie sieht.

**Und wenn gar keine Werkzeuge da sind**, bleibt der Denkansatz, der ohne alles funktioniert: Für jede wichtige Seite zwei Fragen. Wie viele interne Links zeigen darauf, und auf wie viele wichtige Seiten zeigt sie selbst? Das ist Delta im Kopf.

**Der richtige Zeitpunkt für Kevins Vollmodell** wäre, wenn fairbeamtet.de auf mehrere hundert URLs gewachsen ist und Logfiles verfügbar sind.

## Quellen

Einordnung von Kevin Indig als Fachmann: [[SEO-Fachleute und Quellen]].

**Von ihm selbst, frei zugänglich:**
- [Tech SEO Boost 2018: Internal Link Building on Steroids](https://www.slideshare.net/KevinIndig1/kevin-indig-internal-link-building-on-steroids-tech-seo-boost) — die Originalfolien, Quelle für die vier Zutaten, die sechs Schritte, die Rangmethode und die Einschränkungen
- [Revolutionizing Internal Linking](https://www.slideshare.net/KevinIndig1/kevin-indig-revolutionizing-internal-linking) — spätere Fassung
- [Internal Linking for SEO: best practices, strategies, axioms](https://www.growth-memo.com/p/internal-linking-for-seo-best-practices) — frei lesbar, erklärt CheiRank, nennt TIPR
- [X-Thread zum Modell](https://x.com/Kevin_Indig/status/1505983012177121297)

**Hinter der Paywall:**
- [Internal Link Optimization with TIPR](https://www.growth-memo.com/p/internal-link-optimization-with-tipr) — 04.12.2018
- [TIPR lite](https://www.growth-memo.com/p/tipr-lite) — 21.03.2022

**Die praktikabelste Anleitung, frei zugänglich:**
- [Alexander Außermayr: Kevin Indigs TIPR Lite noch leichter](https://aussermayr.com/blog/tipr-lite-interne-verlinkung) — Stand 17.09.2022. Quelle für die Delta-Formel, den Screaming-Frog-Ahrefs-Ablauf und die bewussten Auslassungen. **Werbe-Check:** selbstständiger SEO-Consultant aus Salzburg, verkauft Beratung, kein eigenes Tool. Die genannten Werkzeuge sind Fremdprodukte ohne erkennbare Affiliate-Kennzeichnung.

**Dritte:**
- [Lumar: Webinar-Recap mit Kevin Indig](https://www.lumar.io/webinars-events/webinar-recap-internal-link-building-kevin-indig/) — gute Zusammenfassung des Modells
- [The Blueprint Training, Modul 2.6](https://modules.theblueprint.training/p/courses/module-2-6-internal-linking-optimization/172027-default-section/581035-2-6-1-introduction-to-kevin-indig-s-tipr-model) — lehrt TIPR als Teil eines **kostenpflichtigen Kurses**. Fremdanbieter, der Kevins Modell vermarktet.

**Werbe-Check:** Kevin Indig verkauft kein Tool. Growth Memo ist überwiegend kostenlos, die beiden TIPR-Kernbeiträge sind aber Premium-Inhalte. Das Modell selbst ist frei beschrieben — über seine Konferenzfolien, die jeder einsehen kann.

## Nicht belegt

- Die Zahl **160 % mehr organischer Traffic bei Atlassian** stammt aus einem Webinar-Recap und ist Kevins eigene Fallstudie, nicht unabhängig geprüft.
- Kevins Originalfassung von TIPR lite habe ich wegen der Paywall nicht gelesen. Der Ablauf in dieser Notiz stammt aus Außermayrs frei zugänglicher Umsetzung, nicht aus Kevins Text. Wo beide voneinander abweichen könnten, weiß ich nicht.
- Ob und wie Google intern tatsächlich etwas PageRank-Ähnliches berechnet, ist öffentlich nicht bestätigt. TIPR ist ein **Modell zur Entscheidungsfindung**, keine Rekonstruktion von Googles Algorithmus.
