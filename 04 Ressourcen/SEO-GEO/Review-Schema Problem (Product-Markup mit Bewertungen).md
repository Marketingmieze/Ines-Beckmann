---
tags: [ressource, fairbeamtet, seo, technisch]
erstellt: 2026-10-05
status: offen
---

# Review-Schema Problem: Product-Markup mit Bewertungen

## Worum geht's

Bei einem Check mit dem Rich-Results-/Schema-Validator ist aufgefallen, dass fairbeamtet.de auf jeder Seite ein `Product`-Schema ausgibt, das eigentlich die Firma selbst meint (nicht ein echtes Produkt), zusammen mit einer aggregierten Sternebewertung. Das betrifft vermutlich jede Unterseite der Website, inklusive aller Artikel.

Gefundenes Schema (Beispiel vom Artikel "Pauschale Beihilfe"):

```
@type: Product
name: fairbeamtet.de
description: [Firmenbeschreibung]
image: https://images.provenexpert.com/.../fairbeamtet-de_full_1774264581.jpg
brand: { @type: Brand }
review: {
  @type: Review
  author: { @type: Person, name: "anonym" }
}
aggregateRating: {
  @type: AggregateRating
  bestRating: 5
  ratingValue: 4.86
  reviewCount: 1114
}
```

Das stammt vermutlich automatisch von einem ProvenExpert-Plugin/Widget, das sitebreit eingebunden ist.

## Warum das wichtig ist: Googles "Self-Serving Reviews"-Regel

Google hat (verschärft seit Juli 2026) eine Regel gegen sogenannte "Self-Serving Reviews": Eine Organisation darf ihre eigene aggregierte Bewertung nicht einfach als Schema auf der eigenen Seite ausgeben, wenn die zugrunde liegenden Einzelbewertungen nicht tatsächlich sichtbar und nachprüfbar auf genau dieser Seite stehen.

Konkret verlangt Google:

- Das Schema muss **exakt** dem entsprechen, was auf der Seite sichtbar ist (Zahl der Bewertungen, Inhalt).
- Idealerweise bekommt jede sichtbar angezeigte Bewertung ein eigenes `Review`-Objekt im Code, nicht nur eine pauschale Zahl mit einem generischen Platzhalter.
- Bewertungsplattformen wie ProvenExpert oder Trustindex dürfen die Bewertungen **auf ihrer eigenen Seite** (provenexpert.com, trustindex.io) mit Schema auszeichnen, weil sie die unabhängige Partei sind, die die Bewertungen tatsächlich sammelt. Wir dürfen deren aggregierte Zahl aber nicht einfach unverändert auf unsere eigene Seite kopieren und als unser eigenes Schema ausgeben.

**Wichtige Entwarnung dazu:** Wir bekommen laut Googles eigenen Aussagen **keine Strafe allein dafür**, dass wir Bewertungen/Testimonials auf der Seite zeigen. Das ist grundsätzlich erlaubt und sogar erwünscht. Der eigentliche Auslöser für Probleme ist, wenn das Schema etwas **behauptet, das nicht zur sichtbaren Seite passt** (irreführende strukturierte Daten), nicht die Tatsache, dass wir überhaupt Bewertungen zeigen.

## Was wir aktuell schon richtig machen

Wir haben auf jeder Seite ein Bewertungs-Karussell eingebaut ("So bewerten uns unsere Kunden"), das echte einzelne Bewertungen mit Sternen, Datum und Text zeigt, nicht nur eine nackte Zahl. Das ist genau der Unterschied zwischen "zeigt null Bewertungen" (Googles Negativbeispiel für einen klaren Verstoß) und unserem Fall. Das senkt das Risiko schon deutlich.

## Zwei offene Probleme, die noch behoben werden sollten

### 1. Zwei verschiedene Bewertungsplattformen mit unterschiedlichen Zahlen

Im `Product`-Schema im Code steht eine Bildquelle von **ProvenExpert** mit **4,86 Sternen aus 1.114 Bewertungen**.

Im sichtbaren Karussell auf der Seite steht aber **"Trustindex"** mit **4,9 Sternen aus 1.006 Bewertungen**.

Das sind zwei unterschiedliche Zahlen auf derselben Seite. Das wirkt uneinheitlich und wäre bei einer genaueren Prüfung (durch Google oder auch einfach durch einen aufmerksamen Nutzer) nicht stimmig.

**Wahrscheinlichste Erklärung (Ines' Vermutung, nach Recherche plausibel):** Trustindex ist kein eigenständiges, konkurrierendes Bewertungsportal, sondern ein Sammel-Widget, das Bewertungen von über 100 Plattformen (u. a. Google, Facebook, vermutlich auch ProvenExpert) automatisiert zieht und auf der Website anzeigt. Die Differenz (1.114 vs. 1.006) kommt dadurch wahrscheinlich nicht von zwei konkurrierenden Systemen, sondern entweder von einer Caching-Verzögerung (Trustindex hat die ProvenExpert-Zahl noch nicht neu synchronisiert) oder von einer leicht anderen Berechnungsgrundlage (andere/zusätzliche Quellen einbezogen).

**Frage an Sven/Entwickler, präzisiert:** Zieht sich das Trustindex-Widget seine Zahl automatisch und aktuell von ProvenExpert, oder gibt es einen Cache, der manuell/regelmäßig aktualisiert werden muss? Falls Cache: Wie oft synchronisiert er sich, und lässt sich das beschleunigen oder manuell anstoßen?

### 2. Das Schema selbst zeigt weiterhin nur 1 Review-Objekt statt echter Einzelbewertungen

Im Code steht nach wie vor nur **ein** generisches `Review`-Objekt mit Autor "anonym", während `reviewCount` 1.114 (bzw. laut Karussell 1.006) behauptet. Das sichtbare Karussell zeigt zwar echte Bewertungen für Menschen, aber ob das zugrunde liegende Schema diese auch einzeln als separate `Review`-Objekte im Code abbildet, oder ob der Code weiterhin bei der einen Pauschal-Zeile bleibt, müsste technisch geprüft werden.

**Konkrete Frage an den Entwickler/das Plugin:** Generiert das Trustindex/ProvenExpert-Widget pro angezeigter Bewertung automatisch ein eigenes `Review`-Objekt im strukturierten Daten-Code, so wie es im Karussell sichtbar ist? Oder bleibt der Code unabhängig vom Karussell-Inhalt bei der einen generischen Zeile?

## Mögliche Konsequenzen, falls das nicht behoben wird

Auch wenn die Wahrscheinlichkeit für die schwereren Fälle gering ist, hier alle möglichen Auswirkungen, sortiert nach Wahrscheinlichkeit:

| Konsequenz | Wahrscheinlichkeit | Schwere | Beschreibung |
|---|---|---|---|
| **Keine Sterne im Google-Suchergebnis-Snippet** | Hoch | Gering | Google ignoriert die widersprüchliche Bewertung einfach automatisiert und zeigt keine Sterne neben unserem Link in der Suche. Kein Traffic-Verlust an sich, nur ein verpasster Vertrauens-Bonus in der Trefferliste. |
| **KI-Systeme nutzen unsere Bewertungszahl nicht als Zitat/Vertrauenssignal** | Möglich | Gering | ChatGPT, Perplexity und Google AI Overviews nutzen Bewertungen aktiv als Vertrauenssignal (Perplexity zitiert sie in praktisch 100% der relevanten Antworten). Wenn die KI widersprüchliche Zahlen auf unserer Seite findet, wird sie das vermutlich einfach nicht als verlässliche Quelle für unsere Bewertung nutzen, statt uns aktiv schlechter zu bewerten. Für uns heißt das: verpasstes Potenzial, keine Bestrafung. |
| **Echte manuelle Maßnahme (Manual Action) von Google** | Niedrig | Hoch | Falls Google das Muster als systematisch irreführend einstuft (Schema behauptet etwas, das nicht zur Seite passt), kann das zu einer manuellen Maßnahme führen, die uns die Berechtigung für Rich-Snippets auf der GANZEN Domain entzieht, nicht nur auf einer Seite. |
| **Breitere Spam-Einstufung mit Ranking-Auswirkung** | Sehr niedrig | Sehr hoch | Der seltenste, schwerste Fall: Falls Google das als Teil eines systematischen Täuschungsmusters einstuft, könnte das über reine Rich-Snippet-Entziehung hinausgehen und das Ranking insgesamt beeinträchtigen. Das ist laut Recherche aber eher die Ausnahme bei offensichtlichem, breit angelegtem Missbrauch, nicht bei einer einzelnen technischen Inkonsistenz wie unserer. |

## Warum das für uns trotzdem wichtig ist, auch bei geringer Wahrscheinlichkeit

Unabhängig von der reinen Risiko-Wahrscheinlichkeit: Wir wollen als Marke Vertrauen ausstrahlen, das ist einer unserer Kernwerte (siehe Schreibstil: "Vertrauen über konkrete Zahlen aufbauen, nicht über Behauptungen"). Zwei unterschiedliche Bewertungszahlen auf derselben Website widersprechen genau diesem Prinzip, auch wenn Google oder eine KI es nie bemerken würde, ein aufmerksamer menschlicher Besucher könnte es trotzdem auffallen und als unseriös wahrnehmen. Das ist also auch ein Marken-/Trust-Thema, nicht nur ein technisches SEO-Detail.

## Welche Plattform ist das stärkere Vertrauenssignal: ProvenExpert oder Trustindex?

Recherche-Ergebnis: **ProvenExpert ist klar das stärkere, bekanntere Vertrauenssignal** für unseren Kontext.

- ProvenExpert ist die bekannteste Bewertungsplattform im DACH-Raum speziell für Dienstleister, Berater und Coaches, über 200.000 Unternehmen nutzen sie aktiv, 2,4 Millionen Profile insgesamt. Das ProvenExpert-Siegel wird von Nutzern erkannt und mit Seriosität assoziiert.
- Trustindex ist dagegen eher ein technisches Anzeige-Werkzeug ohne eigene Bekanntheit als Vertrauens-Marke. Es sammelt selbst keine Bewertungen, sondern zieht sie nur von anderen Quellen (auch von ProvenExpert) und zeigt sie an.
- Für unsere Zielgruppe (Beamte, die laut ICP besonders vorsichtig gegenüber unseriösen Angeboten sind) ist ein erkennbares, etabliertes Siegel wie ProvenExpert wertvoller als ein unbekanntes Widget-Tool.

**Empfehlung:** Falls wir uns auf eine sichtbare Quelle konsolidieren, sollte das ProvenExpert sein, sowohl im Schema-Code als auch im sichtbaren Widget auf der Seite. Trustindex kann technisch im Hintergrund bleiben, falls es nur zur Darstellung dient, aber die Marke, die der Nutzer sieht, sollte ProvenExpert sein.

## Nächste Schritte

1. Mit Sven klären: ProvenExpert oder Trustindex, oder beide parallel? Auf eine Quelle konsolidieren.
2. Entwickler/Plugin-Anbieter fragen: Werden die im Karussell sichtbaren Einzelbewertungen auch einzeln im strukturierten Daten-Code (`Review`-Objekte) abgebildet, oder bleibt der Code unabhängig vom Karussell-Inhalt?
3. Nach der Korrektur: Seite erneut durch einen Schema-Validator (z. B. Google Rich Results Test) laufen lassen, um zu prüfen, ob die Diskrepanz behoben ist.

## Quellen

- [developers.google.com – General Structured Data Guidelines](https://developers.google.com/search/docs/appearance/structured-data/sd-policies)
- [jsonschemaapp.com – Google Self-Serving Reviews Rule](https://jsonschemaapp.com/blog/google-self-serving-reviews-rule/)
- [seroundtable.com – Google: Rich Results Manual Actions können zu Spam-Strafen führen](https://www.seroundtable.com/google-penaltes-rich-results-34431.html)
- [trustmary.com – The Impact of Reviews on AI Search in 2026](https://trustmary.com/ai-visibility/the-impact-of-reviews-on-ai-search/)

## Verwandt

- [[04 Ressourcen/SEO-GEO/AI Citations Strategie.md|AI Citations Strategie]]
- [[04 Ressourcen/SEO-GEO/SEO-GEO.md|SEO-GEO]]
