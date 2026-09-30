---
tags:
  - ressource
  - seo
date: 2026-09-27
---

# Mobile UX und Core Web Vitals

Hebel 9 von 10 aus [[Googles No. 1]]. Der einzige Hebel, bei dem Google ausdrücklich davor warnt, ihn zu überoptimieren — und der einzige, den fairbeamtet.de **bereits bestanden hat**. Was bleibt, ist eine Reserve, kein Mangel.

## Wie wichtig das wirklich ist

Google beantwortet die Frage selbst, in der FAQ zur Page Experience:

> **Is there a single „page experience signal" that Google Search uses for ranking?**
> „There is no single signal. Our core ranking systems look at a variety of signals that align with overall page experience."

> **What aspects of page experience are used in ranking?**
> „**Core Web Vitals are used by our ranking systems.** […] Keep in mind that getting good results in reports like Search Console's Core Web Vitals report or third-party tools doesn't guarantee that your pages will rank at the top of Google Search results; there's more to great page experience than Core Web Vitals scores alone. These scores are meant to help you to improve your site for your users overall, and **trying to get a perfect score just for SEO reasons may not be the best use of your time.**"

> „**Beyond Core Web Vitals, other page experience aspects don't directly help your website rank higher in search results.** However, they can make your website more satisfying to use."

Und der Satz, der die Einordnung liefert:

> **How important is page experience to ranking success?**
> „Google Search always seeks to show the most relevant content, **even if the page experience is sub-par**. But for many queries, there is lots of helpful content available. Having a great page experience can contribute to success in Search, in such cases."

**Das ist ein Gleichstandsentscheid, kein Rankingfaktor erster Ordnung.** Wo der Inhalt überlegen ist, gewinnt er auch langsam. Wo mehrere gute Antworten konkurrieren — und das ist bei „Beihilfe Bayern" der Normalfall — kann die Geschwindigkeit den Ausschlag geben.

Gleichzeitig: Von den sechs Selbstprüfungsfragen zur Page Experience sind **Core Web Vitals die einzige, die Google als rankingrelevant bezeichnet.** Der Rest — HTTPS, mobile Darstellung, keine störende Werbung, keine Interstitials, Hauptinhalt klar erkennbar — wirkt nur mittelbar.

**Die Fachwelt setzt den Hebel noch tiefer an.** In der Umfrage von Zyppy, 131 Teilnehmer, landen Core Web Vitals bei **+0,92** — „leicht positiv", im unteren Drittel der Liste. Site Speed liegt mit +1,23 darüber, mobile Bedienbarkeit mit +1,66 deutlich darüber. Ryan Jones dort: „Speed and CWV are the most over-rated things in SEO. Those are literally one of the smallest factors ever." Die Autoren vermerken ausdrücklich, dass es zu diesem Punkt Streit unter den Teilnehmern gab.

Das ist ein Konsenswert, kein Nachweis — Einordnung in [[Ranking-Faktoren-Umfrage 2026]]. **Er deckt sich aber mit Googles eigenem Satz oben**, dass ein perfekter Wert „may not be the best use of your time". Zwei unabhängige Richtungen, dieselbe Aussage. Für fairbeamtet.de heißt das: Der Hebel ist bestanden und bleibt es. Weitere Arbeit daran ist keine Reserve, sondern verlorene Zeit.

Drei Werte aus derselben Umfrage stehen allerdings klar im Negativbereich und gehören hierher: **Popups und Interstitials −1,31, Anzeigendichte −1,31, Inhalt erfordert clientseitiges JavaScript −1,04.** Das ist die Seite der Page Experience, die weh tut — nicht die Millisekunden.

## Die drei Kennzahlen und ihre Schwellen

| Kennzahl | Misst | Gut |
|---|---|---|
| **LCP** — Largest Contentful Paint | Ladeleistung | unter **2,5 s** |
| **INP** — Interaction to Next Paint | Reaktionsfähigkeit | unter **200 ms** |
| **CLS** — Cumulative Layout Shift | Bildstabilität | unter **0,1** |

Zwei Details, die ständig übersehen werden:

> „To ensure you're hitting the recommended target for these metrics for most of your users, a good threshold to measure is **the 75th percentile of page loads, segmented across mobile and desktop devices.**"

> „Tools that assess Core Web Vitals compliance should consider a page passing if it meets the recommended targets at the 75th percentile **for all three** of the Core Web Vitals metrics."

**Es zählt das 75. Perzentil echter Nutzer, nicht der Laborwert**, und es müssen **alle drei** bestehen. Ein Lighthouse-Score von 95 sagt darüber nichts aus — das ist eine Labormessung auf einem simulierten Gerät.

## Mobile First ist keine Empfehlung, sondern die Grundlage

> „Google uses the mobile version of a site's content, crawled with the smartphone agent, for indexing and ranking. This is called mobile-first indexing."

Die wichtigste Regel daraus heißt bei Google schlicht „Make sure that content is the same on desktop and mobile". Wer mobil weniger ausliefert, wird mit weniger bewertet. Googles bevorzugte Bauform:

> „**Responsive design:** Serves the same HTML code on the same URL regardless of the users' device […] Google recommends Responsive Web Design because it's the easiest design pattern to implement and maintain."

## Der Zustand von fairbeamtet.de, gemessen am 27.09.2026

### Das Ergebnis zuerst: alles grün

Sven hat die Felddaten am 27.09.2026 nachgeliefert. **Die Seite besteht die Core Web Vitals, mobil wie am Rechner.**

**Chrome-UX-Bericht, Ursprung, letzte 28 Tage:**

| | Mobil | Computer | Schwelle |
|---|--:|--:|--:|
| **LCP** | **1,2 s** | **1,8 s** | < 2,5 s |
| **INP** | **136 ms** | **66 ms** | < 200 ms |
| **CLS** | **0** | **0,03** | < 0,1 |
| FCP | 1,2 s | 1,4 s | — |
| TTFB | 0,4 s | 0,9 s 🟠 | — |
| **Bewertung** | **bestanden** | **bestanden** | |

**Search Console, Core Web Vitals, 29.06. bis 25.09.2026:**

| | schlechte URLs | zu optimieren | gute URLs |
|---|--:|--:|--:|
| Mobil | **0** | **0** | **181** |
| Computer | **0** | **0** | **181** |

Und zwar **durchgehend über drei Monate**, ohne einen einzigen Ausschlag. Das ist kein Momentwert, das ist ein stabiler Zustand.

Bemerkenswert: **Mobil ist besser als Desktop.** LCP 1,2 s gegen 1,8 s, und der einzige gelbe Wert im ganzen Bericht ist die Serverantwortzeit am Rechner mit 0,9 s.

### Warum das Labor etwas anderes sagt — und warum das Feld recht hat

Dieselbe Seite, dieselbe Minute, Lighthouse 13.5.0:

| | Mobil (Labor) | Computer (Labor) |
|---|--:|--:|
| Leistungsbewertung | **62** 🟠 | **70** 🟠 |
| FCP | 3,4 s 🔴 | 0,5 s |
| LCP | **4,3 s** 🔴 | 0,6 s |
| Total Blocking Time | 530 ms 🟠 | **740 ms** 🔴 |
| CLS | 0 | 0,004 |
| Speed Index | 5,2 s 🟠 | 1,9 s 🟠 |

**Im Labor fällt die Seite durch, im Feld besteht sie.** Der Widerspruch ist keiner. Lighthouse simuliert ein gedrosseltes Mittelklasse-Telefon in einem langsamen Mobilfunknetz, einmalig und ohne Zwischenspeicher. Der Chrome-UX-Bericht misst, was Svens Besucher tatsächlich erleben — mit ihren Geräten, ihren Verbindungen und einem gefüllten Browser-Cache.

**Was für die Bewertung zählt, ist das Feld.** Googles eigene Vorgabe lautet 75. Perzentil echter Nutzer. Der Lighthouse-Punktestand kommt in keiner Rankingaussage von Google vor.

Trotzdem ist der Laborwert nicht wertlos, weil er zeigt, **wo die Reserve liegt**: Eine Total Blocking Time von 530 bis 740 ms ist die messbare Spur der 206 KB Inline-Code. Sie belastet den Haupt-Thread. Im Feld merkt man es kaum — INP 136 ms ist komfortabel unter der 200-ms-Schwelle. Aber der Puffer ist kleiner, als er sein müsste.

**Vorbemerkung zur restlichen Messung:** Das Folgende ist von mir am Quelltext und an den HTTP-Antworten gemessen, ergänzend zu den Felddaten oben.

### Was gut ist

| Prüfpunkt | Befund |
|---|---|
| Responsive | **Mobil und Desktop liefern byteweise dasselbe HTML.** Googles Kernanforderung erfüllt |
| Viewport | `width=device-width, initial-scale=1, maximum-scale=5, viewport-fit=cover` — korrekt, Zoom nicht gesperrt |
| Komprimierung | **Brotli aktiv.** 311 KB Rohtext werden als 65 KB übertragen |
| Statische Dateien | `Cache-Control: public, max-age=2592000` — 30 Tage, bei **allen** 29 Dateien |
| Bilder: `alt` | **Alle** Bilder haben ein `alt`-Attribut. Null Ausreißer |
| Bilder: Lazy Loading | 86 von 89 auf der Startseite, 78 von 81 auf der Hub-Seite |
| Bilder: Maße im Markup | 79 von 89 bzw. 71 von 81 tragen `width` und `height` — das schützt vor Layoutsprüngen, also vor CLS |
| Ladesteuerung | 6 × `preload`/`preconnect`, 1 × `fetchpriority` gesetzt |
| Serverantwort | 158 bis 306 ms |
| Schriften | OMGF im Einsatz, Google Fonts werden also lokal ausgeliefert |

**Das ist kein vernachlässigtes Setup.** Die Handarbeit ist gemacht.

### Das eine große Problem: 66 % jeder Seite sind Inline-Code

Gemessen an `/beihilfestelle-hessen/`, einer Seite mit **548 Wörtern Text**:

| Bestandteil | Größe |
|---|--:|
| HTML gesamt, unkomprimiert | 311 KB |
| davon **Inline-CSS** in **88 einzelnen `<style>`-Blöcken** | 92 KB |
| davon **Inline-JS** in 18 `<script>`-Blöcken | 115 KB |
| **Inline-Anteil zusammen** | **206 KB = 66 %** |

Und hier liegt der Kern: **Inline-Code lässt sich nicht zwischenspeichern.** Die 158 KB an externen CSS- und JS-Dateien lädt der Browser einmal und behält sie 30 Tage. Die 206 KB Inline-Code kommen bei **jedem einzelnen Seitenaufruf** neu über die Leitung. Wer sich drei Bundesland-Seiten ansieht, lädt sie dreimal.

**Die größten Einzelblöcke:**

| Block | Größe | Was es ist |
|---|--:|---|
| `…-js-extra` (Real Cookie Banner Pro) | **69,5 KB** | JSON-Konfiguration des Cookie-Banners |
| `global-styles-inline-css` | 32,5 KB | WordPress-Basisstile aus `theme.json` |
| `fluent-cart-app-js-extra` | 16,1 KB | Konfiguration des Shop-Systems |
| `ugb-style-css-inline-css` | 13,0 KB | Stackable-Blöcke |
| `independent-analytics-script` | 12,4 KB | Statistik-Werkzeug |
| `ugb-style-css-nodep-inline-css` | 8,8 KB | Stackable, zweiter Block |
| Strukturierte Daten (`ld+json`) | 6,4 KB | sinnvoll, bleibt |

**Der Cookie-Banner ist der größte einzelne Posten der ganzen Seite** — größer als jQuery, größer als jedes Bild, größer als der Text um Faktor 20. Auf jeder der 283 Seiten.

### Das zweite Problem: ein Warenkorb auf einer Maklerseite

Auf **jeder** Seite werden geladen:

- `FluentCartApp.js` (7,8 KB) plus 16,1 KB Inline-Konfiguration
- `cart-drawer.css` (3,8 KB)
- `modal-checkout.css` (0,8 KB)
- `toastify-js` und `toastify.css` (4,3 KB)

Zusammen rund **33 KB für ein Shop-System** auf einer Website, die keine Produkte verkauft, sondern Beratungstermine vergibt.

### Kleinere Posten

- **jQuery 31,7 KB plus jquery-migrate 5,1 KB.** `jquery-migrate` ist eine Kompatibilitätsbrücke für veralteten Code und hat in einer Produktivumgebung nichts verloren.
- **29 Dateianfragen** für CSS und JS, darunter **fünf** verschiedene `main.min.css` aus unterschiedlichen Verzeichnissen, vier davon unter 2 KB.
- **1.049 bis 2.086 DOM-Elemente** je Seite. Für 548 Wörter Text ist das viel.
- **Nur 9 bis 19 der Bilder liegen als WebP vor**, der Rest in älteren Formaten.

### Korrektur einer eigenen Angabe

In [[Technische Indexhygiene]] und [[Spam-Richtlinien und Spam-Risiko]] steht, es gebe „kein HTTP-Caching" und das HTML sei mit 310 bis 455 KB aufgebläht. **Beides ist zu pauschal und hiermit richtiggestellt:**

- **Statische Dateien werden sehr wohl 30 Tage zwischengespeichert.** Nur das HTML-Dokument selbst trägt kein `Cache-Control` und kein `ETag` — bei HTML ist das eine vertretbare Entscheidung, es verhindert nur `304`-Antworten.
- **Die 310 bis 455 KB sind der unkomprimierte Rohtext.** Über die Leitung gehen dank Brotli 65 bis 90 KB. Das Problem ist nicht die Übertragungsmenge, sondern dass zwei Drittel davon **bei jedem Aufruf erneut** kommen, weil sie inline stehen.

Die Substanz des Befunds bleibt, die Zahlen waren falsch gerahmt.

## Best Practice für fairbeamtet.de

**Die wichtigste Maßnahme ist, nichts zu überstürzen.** Alle drei Werte sind seit drei Monaten grün, auf 181 von 181 URLs, mobil und am Rechner. Googles eigener Satz gilt hier wörtlich: „trying to get a perfect score just for SEO reasons may not be the best use of your time." **Der Hebel ist erledigt. Die Zeit gehört zurück in den Inhalt.**

Was trotzdem lohnt, weil es die Reserve vergrößert und Besuchern nutzt — nach Wirkung sortiert, alles Konfiguration statt Programmierung. Kein Punkt davon ist dringend.

**1. Den Cookie-Banner aus dem HTML holen.** 69,5 KB inline auf jeder Seite ist der größte Einzelposten — und im Labor-Screenshot ist gut zu sehen, dass der Banner beim ersten Aufbau das halbe Bild füllt. Er ist mit hoher Wahrscheinlichkeit das LCP-Element im Labor. Real Cookie Banner Pro bietet Einstellungen zur Auslieferung der Konfiguration; wenn sie sich als externe, zwischenspeicherbare Datei laden lässt, sind zwei Drittel des Problems erledigt. Falls nicht: Der Hersteller ist der richtige Adressat.

**2. FluentCart klären.** Rund 33 KB je Seite. In der Search Console gibt es einen Abschnitt „Shopping", der Shop ist also vermutlich **nicht** tot — meine erste Einschätzung war voreilig. Die Frage lautet deshalb nicht „abschalten?", sondern: **lädt er nur dort, wo er gebraucht wird?** Bei den meisten Optimierungs-Plugins ist das eine Regel mit zwei Klicks.

**3. `global-styles-inline-css` reduzieren.** 32,5 KB WordPress-Basisstile je Seite sind ein bekanntes Problem des Block-Editors. Lässt sich über `theme.json` eingrenzen oder per Plugin auf das tatsächlich Genutzte reduzieren.

**4. Analytics und `jquery-migrate` prüfen.** 12,4 KB Statistik-Skript inline und eine Kompatibilitätsbrücke, die vermutlich niemand mehr braucht.

**5. Die restlichen Bilder auf WebP oder AVIF.** Von 89 Bildern sind 19 modern. Der Rest ist ein Stapelvorgang.

**6. Erfolg im Feld prüfen, nicht im Labor.** Wenn etwas geändert wird, entscheidet der Core-Web-Vitals-Bericht der Search Console, ob es gewirkt hat — nach etwa 28 Tagen, weil CrUX über diesen Zeitraum mittelt. Der Lighthouse-Punktestand ist kein Erfolgsmaßstab. Er würde sich verbessern, ohne dass ein einziger Besucher etwas merkt.

**7. Den grünen Zustand bewachen.** Der eigentliche Wert des Berichts liegt jetzt in der Überwachung. Ein neues Plugin, ein großes Bild ohne Maße, ein eingebettetes Video — und aus 181 guten URLs werden welche mit Handlungsbedarf. Bei jedem größeren Umbau einmal hinsehen.

## Quellen

Überblick über alle Fachleute mit Werbe-Check: [[SEO-Fachleute und Quellen]].

**Primär:**
- [Understanding page experience in Google Search results](https://developers.google.com/search/docs/appearance/page-experience) — die FAQ mit der Einordnung, wie viel das wirklich zählt
- [Understanding Core Web Vitals and Google search results](https://developers.google.com/search/docs/appearance/core-web-vitals) — die drei Kennzahlen und ihre Schwellen
- [Web Vitals](https://web.dev/articles/vitals) — 75. Perzentil, alle drei müssen bestehen
- [Mobile site and mobile-first indexing best practices](https://developers.google.com/search/docs/crawling-indexing/mobile/mobile-sites-mobile-first-indexing) — Responsive Design als empfohlene Bauform, gleicher Inhalt auf beiden Fassungen

**Praxis:**
- [Jonas Tietgens: 50+ Maßnahmen, WordPress schneller zu machen](https://wp-ninjas.de/wordpress-schneller-machen/), Stand Oktober 2025 — **hier zahlt er sich aus.** Seine Rangfolge deckt sich mit dem Befund: Hosting und Theme zuerst, dann Plugins, die auf jeder Seite laden, erst ganz zum Schluss Minifizierung. Zu Inline-Code rät er ausdrücklich, wo die Wahl besteht, die externe Datei zu nehmen. **Werbe-Check: umfangreich.** Affiliate-Links auf WPSpace, Raidboxes, GeneratePress, WP Rocket, FlyingPress, Borlabs Cache, Shortpixel und OMGF Pro, dazu Wartung, Support, Coaching und Mitgliedschaft. Die Diagnosen sind trotzdem brauchbar, die Produktempfehlungen mit Abstand lesen. **Nebenbei:** fairbeamtet.de setzt OMGF bereits ein, einen seiner Empfehlungen.

**Eigene Messung, 27.09.2026:**
- Auslieferung mit Smartphone- und Desktop-Googlebot-Kennung im Vergleich, Übertragungsgrößen mit gzip und Brotli, Zerlegung des HTML in Inline- und externe Bestandteile, Abruf aller 29 CSS- und JS-Dateien samt `Cache-Control`, Auswertung von `viewport`, `alt`, `loading`, `width`/`height`, `preload` und `fetchpriority`

- **PageSpeed Insights und Search Console**, Screenshots von Sven vom 27.09.2026. Belege liegen in `07 Anhänge/Bilder`:
  - [[PageSpeed Insights Felddaten mobil 2026-09-27.png]] · [[PageSpeed Insights Felddaten Computer 2026-09-27.png]]
  - [[PageSpeed Insights Labor mobil 2026-09-27.png]] · [[PageSpeed Insights Labor Computer 2026-09-27.png]]
  - [[Search Console Core Web Vitals 2026-09-27.png]]

**Nicht verwendet:**
- Die kursierende Zahl, nur rund 44 % der WordPress-Seiten bestünden mobil alle drei Core Web Vitals. Drittanbieterstudie, nicht gegen CrUX geprüft.
- **Jono Alderson**, zum zweiten Mal. Er ist fachlich der Richtige für genau dieses Thema — WordPress-Performance, `global-styles`-Ballast, Web Almanac — aber es gibt keinen abrufbaren Fachartikel von ihm dazu. Seine Substanz steckt in Konferenzvorträgen und Almanac-Kapiteln. Damit ist er als zitierfähige Quelle für diesen Ordner **endgültig ausgeschieden**, so gut er sein mag.

## Offene Punkte

- **Warum ist Desktop langsamer als Mobil?** LCP 1,8 s gegen 1,2 s, TTFB 0,9 s gegen 0,4 s, Labor-TBT 740 ms gegen 530 ms. Ungewöhnlich herum. Eine Erklärung habe ich nicht.
- **Nur 181 von 283 URLs** tauchen im Core-Web-Vitals-Bericht auf. Google wertet nur URLs mit ausreichend Nutzerdaten aus; die übrigen rund 100 sind zu selten besucht. Kein Fehler, aber ein Hinweis darauf, welcher Teil des Bestands kaum Verkehr sieht.
- **Welches Theme läuft?** Die Datei `wdt-custom-avada-js.js` deutet auf Avada hin, ein schwergewichtiges Multifunktions-Theme. Nicht bestätigt.
- **Welches Caching-Plugin ist aktiv?** Ein Kommentar im Quelltext nennt „Speed Optimizer". Die 30-Tage-Header kommen von irgendwo, das gehört aufgeklärt, bevor jemand ein zweites Plugin danebenstellt.
- **Störende Interstitials** habe ich nicht geprüft. Der Cookie-Banner ist rechtlich geboten und zählt nicht dazu, andere Einblendungen wären zu prüfen.
- **Tap-Targets und Schriftgrößen auf dem Telefon** lassen sich am Quelltext nicht beurteilen. Das braucht einen Blick auf einem echten Gerät.
