---
tags:
  - ressource
  - seo
date: 2026-09-27
---

# Technische Indexhygiene

Hebel 8 von 10 aus [[Googles No. 1]]. Der Hebel mit dem schlechtesten Verhältnis von Aufregung zu Wirkung — und trotzdem der, bei dem fairbeamtet.de drei konkrete Baustellen hat.

## Googles eigene Erwartungshaltung

Bevor irgendein Werkzeug angeworfen wird, dieser Satz aus den Search Essentials:

> „The technical requirements cover the bare minimum that Google Search needs from a web page in order to show it in search results. **There are actually very few technical things you need to do to a web page; most sites pass the technical requirements without even realizing it.**"

Das ist die Einordnung, die in Agenturangeboten nie vorkommt. Technisches SEO ist bei einer normalen WordPress-Seite keine Baustelle, sondern eine Hygienefrage. Die Arbeit liegt woanders — bei den Hebeln 1 bis 7.

Und gleich hinterher die Ernüchterung:

> „Just because a page meets all of these requirements and best practices, doesn't mean that Google will crawl, index, or serve its content."

## Crawl-Budget: gilt für uns nicht

Der meistdiskutierte Begriff dieses Hebels ist für fairbeamtet.de **irrelevant**, und das steht so bei Google. Gleich im ersten Absatz des Leitfadens:

> „If your site doesn't have a large number of pages that change rapidly, or if your pages seem to be crawled the same day that they are published, **you don't need to read this guide.** For Google Search specifically, keeping your sitemap up to date and checking the Page Indexing report regularly is adequate."

Die Schwellen, ab denen es überhaupt losgeht:

> - „Large sites (1 million+ unique pages) with content that changes moderately often (once a week)"
> - „Medium or larger sites (10,000+ unique pages) with very rapidly changing content (daily)"
> - „Sites with a large portion of their total URLs classified by Search Console as Discovered - currently not indexed"

fairbeamtet.de hat **283 URLs** und **fünf** Seiten im Status „Discovered – currently not indexed". Keine der drei Bedingungen ist erfüllt, nicht annähernd. **Wer hier über Crawl-Budget redet, verkauft etwas.**

Ein Satz aus dem Leitfaden bleibt trotzdem wichtig, weil er Hebel 8 mit dem Rest verbindet:

> „Google determines the crawling resources allocated to each site by factoring in elements that are relevant to the specific Google product. For example, for Google Search, this includes things like popularity, overall user value, **content uniqueness**, and serving capacity."

Crawl-Frequenz ist also ein *Ergebnis* von Qualität, kein Regler, an dem man dreht.

## Die Asymmetrie: verlieren ja, gewinnen nein

Die Umfrage von Zyppy bildet diesen Hebel besser ab als jede andere Quelle, weil sie beide Enden zeigt. In der offenen Frage nach den drei wichtigsten Faktoren landet technische SEO-Gesundheit auf **Platz 8 mit 17,5 %** — Mittelfeld. Der **stärkste Negativwert der gesamten Umfrage** ist dagegen technisch: **von robots.txt blockiert, −2,22.** Marshall Simmonds dort: „Tech SEO is a commodity at this point. It won't necessarily win the race, but it can absolutely lose it."

Die technischen Werte im Einzelnen, Konsenswerte aus [[Ranking-Faktoren-Umfrage 2026]]:

| | Wert |
|---|---|
| Zugang für KI-Crawler und Snippet-Freigabe | +2,20 |
| Korrekte Canonicals | +1,56 |
| HTTPS | +1,28 |
| Crawl-Frequenz | +1,06 |
| Korrektes Hreflang | +1,02 |
| URL in der XML-Sitemap | +0,80 |
| HTML-/W3C-Validierung | +0,38 |
| URL-Länge | +0,08 |
| Inhalt erfordert clientseitiges JavaScript | −1,04 |
| Duplicate Content | −1,19 |
| Verwaiste Seite | −1,79 |
| **Von robots.txt blockiert** | **−2,22** |

**Lies die Tabelle von unten.** Oben steht nichts, was ein Ranking macht. Unten steht alles, was eins verhindert. Genau so ist dieser Hebel zu behandeln: als Prüfliste, die einmal abgehakt wird, nicht als Arbeitsfeld.

Der einzige Wert oben, der echten Zugewinn verspricht, ist **der Zugang für KI-Crawler samt Snippet-Freigabe mit +2,20** — und der ist ebenfalls eine Ja-oder-nein-Frage, kein Optimierungsthema. Einzelheiten in [[SERP AI und Conversion-Optimierung]].

## Die Kennzahl, die stattdessen zählt: Crawl Efficacy

**Jes Scholz** hat dafür den brauchbarsten Begriff geprägt. Ihr Artikel ist am 14.06.2023 erschienen und am 05.12.2025 aktualisiert worden, also aktuell gepflegt.

Ihre Abrechnung mit dem Crawl-Budget:

> „SEO pros often look to crawl budget […] But the idea that more crawling is inherently better is completely misguided. **The total number of crawls is nothing but a vanity metric.** Enticing 10 times the number of crawls per day doesn't necessarily correlate against faster (re)indexing of content you care about. All it correlates with is putting more load on your servers, costing you more money."

Und die Alternative:

> „Quality crawling means **reducing the time between publishing or making significant updates to an SEO-relevant page and the next visit by Googlebot. This delay is the crawl efficacy.**"

**Wie man das ohne Logfiles misst** — und das ist der Teil, der für uns zählt, weil wir keinen Logfile-Zugriff brauchen:

> „If this is not possible, you could consider calculating it using the **lastmod date in the XML sitemaps** and periodically query the relevant URLs with the **Search Console URL Inspection API** until it returns a last crawl status."

Das ist mit Rank Math und der Search Console machbar. **Voraussetzung ist allerdings, dass `lastmod` die Wahrheit sagt** — und genau da hakt es bei uns, siehe unten.

### Ihre fünf Maßnahmen, in ihrer Reihenfolge

1. **Schneller, gesunder Server.** Ihre Zielwerte: Host-Status in der Search Console grün, 5xx-Fehler unter 1 %, Antwortzeiten unter **300 Millisekunden**.
2. **Wertlosen Inhalt entfernen.** „When a significant portion of a website's content is low quality, outdated, or duplicated, it diverts crawlers from visiting new or recently updated content as well as contributes to index bloat." Einstieg: der Filter „Crawled – currently not indexed" in der Search Console, dort nach Ordnermustern suchen, dann zusammenlegen per 301 oder löschen per 404.
3. **Googlebot sagen, was er *nicht* crawlen soll.** „While rel=canonical links and noindex tags are effective at keeping the Google index of your website clean, **they cost you in crawling.**"
4. **Sagen, was und wann.** Eine XML-Sitemap, die sich dynamisch aktualisiert und ein ehrliches Änderungsdatum trägt.
5. **Interne Verlinkung.** „Crawling can only occur through links." Besonderes Augenmerk auf mobile Navigation, Breadcrumbs und verwandte Inhalte — „ensuring none are dependent upon Javascript". Deckt sich mit [[Interne Verlinkung und Informationsarchitektur]].

## Die drei Werkzeuge und ihre Rangfolge

### Canonical

Google nennt die Signalstärke ausdrücklich, in dieser Reihenfolge:

> - „**Redirects:** A strong signal that the target of the redirect should become canonical."
> - „**`rel="canonical"` link annotations:** A strong signal that the specified URL should become canonical."
> - „**Sitemap inclusion:** A weak signal that helps the URLs that are included in a sitemap become canonical."

Und die Entwarnung:

> „While we encourage you to use these methods, **none of them are required; your site will likely do just fine without specifying a canonical preference.**"

Die Fehler, die Google ausdrücklich benennt:

> - „Don't use the robots.txt file for canonicalization purposes. Google may still index URLs that are disallowed in robots.txt without their content."
> - „Don't specify different URLs as canonical for the same page using different canonicalization techniques."
> - „Do include a `rel="canonical"` link on the canonical page itself (also known as a self-referential canonical)."
> - „When linking within your site, link to the canonical URL rather than a duplicate URL."

### noindex

> „Do not show this page, media, or resource in search results."

Wichtig ist, was `noindex` **nicht** tut: Es spart kein Crawling. Aus dem Crawl-Budget-Leitfaden:

> „**Don't use `noindex`**, as Google will still request, but then drop the page when it sees a `noindex` meta tag or header in the HTTP response, **wasting crawling time**."

### Die Falle, in die fast jeder tappt

> „robots meta tags and X-Robots-Tag HTTP headers are discovered when a URL is crawled. **If a page is disallowed from crawling through the robots.txt file, then any information about indexing or serving rules will not be found and will therefore be ignored.** If indexing or serving rules must be followed, the URLs containing those rules cannot be disallowed from crawling."

Im Klartext: **`robots.txt` und `noindex` zusammen heben sich gegenseitig auf.** Wer eine Seite per `robots.txt` sperrt und zusätzlich auf `noindex` setzt, erreicht, dass Google das `noindex` nie sieht — und die URL unter Umständen ohne Inhalt trotzdem indexiert. Entweder das eine oder das andere.

Die Entscheidungsregel, die daraus folgt:

| Ziel | Werkzeug |
|---|---|
| Soll gar nicht erst gecrawlt werden | `robots.txt` Disallow |
| Darf gecrawlt, aber nicht angezeigt werden | `noindex`, **nicht** zusätzlich sperren |
| Ist ein Duplikat, das Signale abgeben soll | `rel="canonical"` |
| Ist dauerhaft weg | 404 oder 410 |
| Ist umgezogen | 301 |

Zu 404 sagt Google übrigens etwas, das der Intuition widerspricht:

> „Google won't forget a URL that it knows about, but a 404 status code is a strong signal not to crawl that URL again. **Blocked URLs, however, will stay part of your crawl queue much longer**, and will be recrawled when the block is removed."

### `lastmod` muss wahr sein

> „Google uses the `<lastmod>` value **if it's consistently and verifiably** (for example by comparing to the last modification of the page) **accurate.** The `<lastmod>` value should reflect the date and time of the **last significant update** to the page. For example, an update to the main content, the structured data, or links on the page is generally considered significant, however an update to the copyright date is not."

Ein `lastmod`, dem Google nicht glaubt, wird ignoriert. Dann ist es nicht neutral, sondern wertlos.

## Der Zustand von fairbeamtet.de, gemessen am 27.09.2026

### Was sauber ist — und das ist das meiste

| Prüfpunkt | Befund |
|---|---|
| Indexabdeckung | 266 von 278 Seiten indexiert, **95,7 %** |
| „Crawled – currently not indexed" | 2 Seiten |
| „Discovered – currently not indexed" | 5 Seiten |
| `robots.txt` | Sauber. Nur `/wp-admin/` gesperrt, `admin-ajax.php` freigegeben, Sitemap verlinkt |
| KI-Crawler | GPTBot, ClaudeBot, PerplexityBot, Google-Extended ausdrücklich erlaubt |
| Canonical | Selbstreferenziell und korrekt gesetzt |
| Parameter-URLs | `?utm_source=…` zeigt sauber auf die Klartext-URL |
| Großschreibung | `/Beihilfe/` liefert 200, kanonisiert aber auf `/beihilfe/` |
| Suchergebnisse `?s=` | `noindex` |
| Kategorie-Blätterseiten | `noindex` |
| Datumsarchiv `/2026/` | 301 auf die Startseite |
| AMP | Nicht vorhanden |
| 404 | Echter 404-Statuscode, kein Soft-404 |
| HTTPS | Erzwungen |
| Strukturierte Daten | BlogPosting, BreadcrumbList, Person, Place, PostalAddress, GeoCoordinates, WebSite |
| Serverantwort | 158 bis 306 ms, nginx |
| `hreflang` | Fehlt, korrekt so — einsprachige Seite |

**Das ist ein gut gepflegtes Rank-Math-Setup.** Die Punkte, an denen sich technisches SEO üblicherweise abarbeitet, sind erledigt.

### Was offen ist, nach Wirkung sortiert

**1. Drei indexierbare URLs pro Person.** Der deutlichste Befund. Für jeden Mitarbeiter existieren bis zu drei indexierbare Seiten:

| Art | Beispiel Michael Buchholz | Umfang |
|---|---|--:|
| Beitrag | `/michael-buchholz-pkv-experte-fairbeamtet/` | rund 1.900 Wörter |
| Pflichtangabe | `/erstinformation/michael-buchholz/` | rund 500 Wörter |
| Autorenarchiv | **`/author/bond-007/`** | rund 1.300 Wörter |

Insgesamt 11 Experten-Beiträge, 8 Erstinformationsseiten und 4 Autorenarchive. Zwei der Autorenarchive tragen technische Benutzernamen als URL: **`/author/bond-007/`** ist Michael Buchholz, **`/author/fairbeamtet/`** ist ein Sammelkonto. Beide sind auf `index, follow` gesetzt, stehen in der Autoren-Sitemap und haben **keine H1**.

Das ist nicht nur Indexhygiene. Es arbeitet direkt gegen [[Trust und E-E-A-T-System]]: Google führt Personen als Entitäten zusammen, und wir zerlegen jeden Experten in drei URLs, von denen eine „bond-007" heißt. Wer die Autorität einer Person aufbauen will, gibt ihr **eine** Adresse.

**2. Dem HTML-Dokument fehlt `ETag`.** *(Korrigiert am 27.09.2026, siehe [[Mobile UX und Core Web Vitals]]: Die statischen Dateien werden sehr wohl 30 Tage zwischengespeichert — `Cache-Control: public, max-age=2592000` bei allen 29 CSS- und JS-Dateien. Betroffen ist nur das HTML-Dokument selbst.)* Das Dokument liefert weder `Cache-Control` noch `ETag`. Damit kann der Server keine `304 Not Modified` beantworten. Google empfiehlt das ausdrücklich:

> „Use HTTP caching: Support 304 (Not Modified) HTTP status codes. If a page hasn't changed since Google last crawled it, returning a 304 code tells Google to reuse the cached version, saving your server bandwidth and resources."

Bei 283 URLs ist das kein Crawling-Problem. Es ist ein Geschwindigkeits- und Wiederbesuchsthema und gehört zu Hebel 9 mit dazu.

**3. `lastmod` sagt nicht die Wahrheit.** In der ersten Beitrags-Sitemap tragen **120 von 200 Beiträgen dasselbe Datum: 27.04.2026.** Das ist kein Redaktionsdatum, das ist eine Sammeländerung — ein Plugin-Update, eine Umstellung, ein Suchen-und-Ersetzen. Nach Googles Maßstab ist das nicht „verifiably accurate", und damit fällt das Signal weg.

Praktische Folge: **Solange `lastmod` lügt, lässt sich die Crawl Efficacy nach Scholz nicht messen**, weil ihr Behelfsweg ohne Logfiles genau auf diesem Feld aufsetzt.

**4. Zwei Sprünge bei der Weiterleitung.** `http://fairbeamtet.de/` → `https://fairbeamtet.de/` → `https://www.fairbeamtet.de/`. Google rät zu kurzen Ketten. Zwei Sprünge sind unkritisch, aber in einem Schritt auf das Ziel wäre sauberer. Betrifft nur Direkteingaben und alte Links.

**5. Drei Seiten seit über 90 Tagen nicht gecrawlt.** `pflegeleistungen-beihilfe-rheinland-pfalz`, `pkv-beratung-kinder`, `beihilfebemessungssatz-berlin`. Bei einer 283-URL-Seite ist das ein Signal für geringe wahrgenommene Wichtigkeit — meist zu wenig interne Links. Verbindung zu Hebel 7.

**6. Der Feed ist indexierbar.** `/feed/` liefert 200 ohne `noindex`. Google kommt damit üblicherweise klar. Kosmetik.

## Best Practice für fairbeamtet.de

**Eine Person, eine URL.** Für jeden Experten eine kanonische Adresse festlegen — sinnvollerweise der ausführliche Beitrag. Die Autorenarchive zeigen per `rel="canonical"` dorthin oder werden per Rank Math auf `noindex` gesetzt. Die Erstinformation bleibt eigenständig, weil sie eine aufsichtsrechtliche Pflichtangabe ist und einen anderen Zweck erfüllt; sie sollte aber sichtbar auf die Personenseite verlinken.

**Der Rank-Math-Fehler ist Geschichte, aber lehrreich.** Am 06.03.2026 wurde ein `noindex` korrigiert, das Rank Math auf der Autorenseite von Sven gesetzt hatte — 21 URLs waren betroffen, siehe das Änderungsprotokoll in [[Sichtbarkeitsverlauf und Relaunch]]. Vorher: null Impressionen. Nachher: 126. **Eine Seite, die auf `noindex` steht, ist nicht schwach, sondern unsichtbar**, und in keiner Sichtbarkeitsauswertung taucht sie als Problem auf — sie fehlt einfach. Nach jedem Plugin-Update und jedem Relaunch gehört der Indexstatus der wichtigen Seitentypen einmal durchgesehen.

**Benutzernamen sind keine URLs.** `bond-007` und `fairbeamtet` als Autoren-Slug gehören korrigiert oder aus dem Index genommen. Ein Autoren-Slug, der nicht der Name ist, hilft niemandem.

**`lastmod` wieder ehrlich machen.** Eine Sammeländerung darf das Änderungsdatum nicht anfassen. Wenn Rank Math das aus `post_modified` zieht, muss bei technischen Massenänderungen `post_modified` unangetastet bleiben. Danach ist das Feld wieder brauchbar — und erst danach lohnt es, Crawl Efficacy überhaupt zu messen.

**`Cache-Control` und `ETag` setzen.** Aufgabe für den Hoster oder ein Caching-Plugin, kein SEO-Thema im engeren Sinn. Wirkt für Besucher wie für Googlebot.

**Nicht mehr sperren als nötig.** Die `robots.txt` ist heute gut. Sie soll so bleiben. Jede zusätzliche Disallow-Zeile ist ein Risiko, weil sie `noindex` und `canonical` blind macht.

**Verwaiste und selten gecrawlte Seiten über interne Links einbinden**, nicht über Sitemap-Tricks. Die Sitemap ist laut Google nur ein schwaches Signal, interne Links sind das starke.

**Einfach crawlbar bleiben, nicht nur crawlbar sein.** Je weniger ein Crawler auflösen muss — Weiterleitungsketten, nachgeladene Inhalte, Parameter, Dubletten mit und ohne Slash —, desto zuverlässiger wird der Inhalt erfasst, und das gilt für Googlebot und für KI-Crawler gleichermaßen. Quelle: Sven Höhne, 30.09.2026. Gestützt wird die Richtung von zwei Werten aus [[Ranking-Faktoren-Umfrage 2026]]: Inhalt, der clientseitiges JavaScript erfordert, steht bei −1,04, Weiterleitungsketten bei −0,93. **Der konkrete Anwendungsfall liegt hier schon auf dem Tisch:** die Slash-Dubletten aus [[Beihilfe-System Bestandsaufnahme]], bei denen dieselbe Seite unter zwei Adressen rankt und sich die Signale nimmt.

**Keine Werkzeuge kaufen, die ein Problem lösen, das wir nicht haben.** Crawl-Budget-Optimierung, Log-File-Analyse und Indexierungs-APIs sind bei 283 URLs vergeudetes Geld. Zur Indexing API sagt Scholz deutlich: Für Seiten ohne `JobPosting`- oder `BroadcastEvent`-Markup „does nothing except add unnecessary load on your server and wastes development resources for no gain".

## Quellen

Überblick über alle Fachleute mit Werbe-Check: [[SEO-Fachleute und Quellen]].

**Primär:**
- [Google Search Essentials](https://developers.google.com/search/docs/essentials) — technische Mindestanforderungen
- [Optimize your crawl budget](https://developers.google.com/search/docs/crawling-indexing/large-site-managing-crawl-budget) — Schwellen, Best Practices, `noindex`-Warnung
- [How to specify a canonical URL](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls) — Signalstärken und Fehlerliste
- [Robots meta tag specifications](https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag) — `noindex`, und die Kombination mit `robots.txt`
- [Build and submit a sitemap](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap) — `lastmod` muss „verifiably accurate" sein

**Praxis:**
- [Jes Scholz: Website Crawling — The What, Why & How To Optimize](https://www.searchenginejournal.com/website-crawling/485275/), Search Engine Journal, veröffentlicht 14.06.2023, aktualisiert 05.12.2025 — Crawl Efficacy als Kennzahl, fünf Maßnahmen. **Werbe-Check:** Beraterin, kein Produkt, keine Affiliate-Links im Beitrag.
- [Jonas Tietgens: Duplicate Content in WordPress](https://wp-ninjas.de/duplicate-content/) — aus 2017, auf Yoast bezogen, empfiehlt `noindex` für Autoren- und Datumsarchive. **Werbe-Check:** bewirbt Coaching, Mitgliedschaft und Support. Der Grundgedanke stimmt, die Umsetzung ist veraltet — die Seite läuft auf Rank Math.

**Eigene Messung, 27.09.2026:**
- `robots.txt`, Sitemaps, Weiterleitungsketten, HTTP-Kopfzeilen, Canonical- und Robots-Angaben, strukturierte Daten, 404-Verhalten, Antwortzeiten
- Search Console über SEO Gets: Indexstatus, zuletzt gecrawlt

**Nicht verwendet:**
- [Jes Scholz: Crawl efficacy — How to level up crawl optimization](https://searchengineland.com/crawl-efficacy-optimization-389085), Search Engine Land — **von Cloudflare blockiert**, nicht abrufbar. Der Inhalt deckt sich laut Suchtreffern mit dem SEJ-Beitrag, der als Quelle dient.
- **Jono Alderson** war der naheliegende Fachmann für diesen Hebel, und hier ist die Fehlanzeige aus [[Interne Verlinkung und Informationsarchitektur]] aufzulösen: Seine Beiträge des Jahres 2026 behandeln Strategie und Organisation, nicht Technik. Seine technische Substanz steckt in Web-Almanac-Kapiteln und Konferenzvorträgen, nicht in abrufbaren Fachartikeln. **Zusatz für den Werbe-Check:** Er arbeitet derzeit über Magnit bei Meta — ein Arbeitgeberinteresse, das nach der Regel aus [[Googles No. 1]] dazugehört.
- **Jannik Schubert** hat zu Indexierung und Crawling nichts. Seine Themen sind Suchintention, Textlänge, Title Tags, interne Verlinkung. Bei Hebel 8 fällt er aus.

## Offene Punkte

- **Akkordeons und Tabs im Page-Builder** noch nicht darauf geprüft, ob Inhalt per CSS versteckt wird. Gehört zusammen mit dem Punkt aus [[Spam-Richtlinien und Spam-Risiko]] erledigt.
- **Host-Status und 5xx-Quote** in der Search Console noch nicht angesehen. Scholz' Zielwerte: grün und unter 1 %.
- **Welche fünf Seiten** stehen auf „Discovered – currently not indexed" und welche zwei auf „Crawled – currently not indexed"? Die Zahlen habe ich, die URLs nicht. Der Filter in der Search Console zeigt sie.
- **Ob Rank Math die Autorenarchive** überhaupt auf `noindex` stellen kann, ohne die Personenseiten zu beeinträchtigen — ungeprüft.
- **Core Web Vitals und das aufgeblähte HTML** (290 bis 454 KB je Seite) gehören zu Hebel 9.
