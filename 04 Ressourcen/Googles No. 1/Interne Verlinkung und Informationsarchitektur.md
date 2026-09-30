---
tags:
  - ressource
  - seo
date: 2026-09-27
---

# Interne Verlinkung und Informationsarchitektur

Hebel 7 von 10 aus [[Googles No. 1]]. Der Hebel, der die anderen verbindet — und der einzige, den man vollständig selbst kontrolliert.

## Warum Links überhaupt zählen

Aus dem SEO Starter Guide, Stand 10.12.2025:

> „In fact, the vast majority of the new pages Google finds every day are through links."

Das gilt für externe wie interne Links. Eine Seite, auf die nichts zeigt, existiert für Google praktisch nicht — unabhängig davon, wie gut sie ist.

## Die technische Mindestbedingung

Aus Googles Dokumentation zu crawlbaren Links, ebenfalls Stand 10.12.2025:

> „Google can only crawl your link if it's an `<a>` HTML element (also known as anchor element) with an `href` attribute."

Das `href` muss „resolves into an actual web address (meaning, it resembles a URI)" enthalten.

**Funktioniert:**
```html
<a href="https://example.com">
<a href="/beihilfe/nrw">
<a href="./beihilfe/nrw">
```
Zusätzliche Attribute wie `onclick` oder `class` stören nicht, dynamisch eingefügte Links auch nicht, solange das Markup stimmt.

**Funktioniert nicht:**
```html
<span href="https://example.com">
<a onclick="goto('https://example.com')">
<a routerLink="produkte/kategorie">
<a href="javascript:goTo('produkte')">
```

Für eine WordPress-Seite ist das selten ein Problem, bei JavaScript-lastigen Seitenbaukästen und Slidern aber schon. Wenn ein Menü per JavaScript aufgebaut wird und keine echten `<a href>` hinterlässt, ist der ganze Zweig unsichtbar.

## Navigation ist bei Google „Supplementary Content"

Die General Guidelines vom 11.09.2025 teilen jede Seite in drei Teile: Hauptinhalt, Supplementary Content und Werbung. Zu SC in Abschnitt 2.4.2:

> „Supplementary Content contributes to a good user experience on the page, but does not directly help the page achieve its purpose. SC is an important part of the user experience. **One common type of SC is navigation links that allow users to visit other parts of the website.**"

Und zur Bewertung:

> „Supplementary Content (SC) is also important. SC can help a page better achieve its purpose **or it can detract from the overall experience**."

Navigation ist also bewertungsrelevant — in beide Richtungen. Zu viel, zu unübersichtlich oder irreführend zieht die Seite nach unten.

**Die harte Grenze** steht bei den Lowest-Beispielen:

> „Pages that disguise Ads as website navigation links. For example, fake directory pages that look like navigation but are actually advertising."

Wer Werbung als Navigation tarnt, bekommt die schlechteste Bewertung. Das ist kein Graubereich.

## Der überraschende Satz

Beim Auffinden der Startseite schreibt Google an seine Prüfer:

> „Sometimes, you may be given a webpage or website that appears to have no navigation links, no homepage link, and no logo or other means to find the homepage. **Even some High or Highest quality pages lack a way to navigate to the homepage.**"

**Fehlende Navigation ist kein automatischer Abwertungsgrund.** Das relativiert einiges, was in der Branche als Pflicht verkauft wird. Eine hervorragende Einzelseite bleibt hervorragend, auch wenn sie schlecht eingebunden ist.

Aber: Sie wird schlechter gefunden, und sie profitiert nicht vom Rest der Website. Der Schaden liegt nicht in der Bewertung, sondern in der Sichtbarkeit.

## Ankertext

Aus dem SEO Starter Guide:

> „Link text (also known as anchor text) is the text part of a link that you can see. **This text tells users and Google something about the page you're linking to.**"

Google empfiehlt außerdem, auf thematisch verwandte Inhalte zu verlinken — das gibt Nutzern und Suchmaschinen Kontext und zeigt Themenkompetenz. Warnung im selben Abschnitt: nicht blind auf nicht vertrauenswürdige Quellen verlinken, sonst `nofollow` setzen.

### Der wichtige Unterschied zu externen Links

Jannik Schubert macht einen Punkt, der oft untergeht: **Interne Ankertexte dürfen hart optimiert werden.** Bei Backlinks ist überoptimierter Ankertext ein Spam-Signal, intern nicht — du bestimmst deine eigene Struktur, das ist kein Manipulationsversuch.

Seine Regeln:

- Keine nichtssagenden Anker wie „hier" oder „zur Seite"
- **Nie denselben Ankertext für verschiedene Zielseiten** verwenden
- Neue Inhalte von **mindestens drei bis fünf** bestehenden Seiten verlinken
- Verwaiste Seiten und Seiten mit kaum internen Links aufspüren und einbinden
- Von starken Seiten (viele Backlinks, viel Traffic) auf schwächere verlinken, um sie zu stützen

Der zweite Punkt ist der wichtigste. Wenn „PKV für Beamte" mal auf die Hub-Seite und mal auf den Beihilfe-Artikel zeigt, weiß Google nicht, welche Seite gemeint ist — und du hast dir das Problem gebaut, das man sonst Kannibalisierung nennt.

## Klicktiefe

Hier wird die Quellenlage dünn, und das gehört gesagt.

Vielfach zitiert wird John Mueller sinngemäß mit: Was von der Startseite verlinkt ist, gilt als wichtiger als das, was fünf oder sechs Schritte entfernt liegt. **Ich habe die Originalquelle nicht gefunden** — die Aussage kursiert in SEO-Blogs, stammt aus einem Webmaster-Hangout und ist mehrere Jahre alt. Sie klingt plausibel und deckt sich mit dem, was Google zur Auffindbarkeit über Links sagt, aber sie ist hier nicht belegt.

Ebenso kursiert die Zahl, ab 50 Links pro Seite falle der Traffic. **Das ist eine Drittstudie ohne Primärquelle**, keine Google-Aussage.

Was belegt ist: Mueller rät zu Auswahl statt Vollständigkeit. Alles von der Startseite zu verlinken bringt nichts, ein paar wirklich wichtige Seiten dort zu verlinken schon.

## Hub und Cluster

Das Modell steht in [[Search Intent und Haupt-Hub]] und [[Topical Authority ohne Kannibalisierung]]. Hier der Teil, der die Verlinkung betrifft.

Jannik Schubert beschreibt „Hub & Spokes" sauber: Die Hub-Seite verlinkt auf die Unterthemen, **und die Unterthemen verlinken zurück auf den Hub**. Erst dadurch entsteht ein Netz statt eines Baums.

Der Rückweg wird fast immer vergessen. Ohne ihn fließt die Stärke nur nach außen und sammelt sich nirgends.

**Werbe-Check:** Der Beitrag empfiehlt das WordPress-Plugin Link Whisper über einen Affiliate-Link. Die Regeln funktionieren ohne jedes Plugin.

## Vertiefung: das TIPR-Modell

Wer interne Verlinkung nach Zahlen statt nach Gefühl steuern will, landet bei Kevin Indigs TIPR-Modell — internem PageRank, CheiRank und Backlinks in einer Rangfolge. Eigene Notiz: [[TIPR-Modell von Kevin Indig]].

Kurzfassung: Für fairbeamtet.de ist das Rechenmodell derzeit zu groß, der Denkansatz aber sofort nutzbar. Zu jeder wichtigen Seite gehören zwei Fragen — was kommt an internen Links herein, und was gibt sie an wichtige Seiten weiter?

## Best Practice für fairbeamtet.de

**Jede Seite braucht einen Absender und einen Rückweg.**
Von wo kommt man auf die Seite, und wohin führt sie zurück? Wenn eine der beiden Fragen unbeantwortet ist, hängt die Seite in der Luft.

**Ankertexte einmal festlegen und durchhalten.**
Eine Liste anlegen: Welcher Ankertext zeigt auf welche Seite? „PKV für Beamte" immer auf den Hub, „Beihilfe NRW" immer auf die Landesseite. Ein Ankertext, ein Ziel.

**Beim Veröffentlichen rückwärts verlinken.**
Neuer Artikel heißt: drei bis fünf bestehende Seiten suchen, in denen er inhaltlich passt, und dort verlinken. Nicht umgekehrt — der neue Artikel verlinkt ohnehin nach außen.

**Verwaiste Seiten aufspüren — vorrangig.**
Seiten ohne eingehende interne Links werden schlechter gefunden und erben keine Stärke. In der Umfrage von Zyppy ist die verwaiste Seite mit **−1,79 der zweitschlechteste Wert der gesamten Liste**, schlechter als Duplicate Content (−1,19) und als spammige Backlinks (−1,26). Konsenswert, kein Nachweis, Einordnung in [[Ranking-Faktoren-Umfrage 2026]] — aber er hebt diesen Punkt aus der Bestandsprüfung nach vorn.

**Qualität der Absender vor Anzahl der Links.**
Dieselbe Umfrage trennt zwei Dinge, die oft in einen Topf geworfen werden: die **Autorität der intern verlinkenden Seiten** steht bei **+1,92**, die **Anzahl interner Links** auf eine URL nur bei +1,49, die Vielfalt der Ankertexte bei +0,91. Ein Link von einer starken Seite wiegt mehr als fünf von schwachen. Das deckt sich mit dem Denkansatz aus [[TIPR-Modell von Kevin Indig]] und mit Muellers Rat zur Auswahl statt Vollständigkeit.

**Starke Seiten als Verteiler nutzen.**
Wenn eine Seite Backlinks oder Traffic hat, ist sie der beste Ort, um eine neue oder schwache Seite zu verlinken.

**Die technische Prüfung nicht vergessen.**
Sind alle Menüpunkte echte `<a href>`? Ein Klick mit deaktiviertem JavaScript oder ein Blick in den Quelltext klärt das in zwei Minuten. Bei WordPress mit Standard-Menüs ist es fast immer in Ordnung, bei Page-Buildern und Mega-Menüs nicht immer.

**Navigation schlank halten.**
Google zählt sie als Supplementary Content, und SC kann die Seite auch verschlechtern. Ein Menü, das alles zeigt, zeigt nichts.

**Nicht überoptimieren.**
Interne Ankertexte dürfen klar sein, aber ein Artikel, in dem jeder dritte Satz einen Link auf dieselbe Geldseite trägt, liest sich wie eine Linkfarm. Der Maßstab bleibt der Leser.

## Quellen

Überblick über alle Fachleute mit Werbe-Check: [[SEO-Fachleute und Quellen]].

**Primär:**
- [Search Quality Rater Guidelines, 11.09.2025](https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf) — 2.4.2 (Supplementary Content), 2.5.1 (Startseite finden), Lowest-Beispiele zu getarnter Navigation
- [Make your links crawlable](https://developers.google.com/search/docs/crawling-indexing/links-crawlable) — Stand 10.12.2025, `<a href>` als Mindestbedingung
- [SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) — Stand 10.12.2025, Ankertext und Auffindbarkeit über Links

**Praxis:**
- [Jannik Schubert: Interne Verlinkung](https://stoplooking.de/interne-verlinkung-ratgeber/) — die konkretesten Regeln, die ich gefunden habe. **Werbe-Check:** Affiliate-Link auf Link Whisper.

**Nicht verwendet:**
- Die vielzitierte Mueller-Aussage zur Klicktiefe („fünf oder sechs Schritte von der Startseite") — Originalquelle nicht auffindbar, stammt aus einem älteren Webmaster-Hangout.
- Die Angabe, ab 50 internen Links pro Seite falle der Traffic — Drittstudie ohne Primärquelle.

## Offene Punkte

- **Jono Alderson** ist der naheliegende Fachmann für diesen Hebel (technisches SEO, WordPress, Informationsarchitektur), aber ich habe keinen konkreten Beitrag von ihm speziell zu interner Verlinkung gefunden. Sein [Blog](https://www.jonoalderson.com/blog/) wäre bei Hebel 8 und 9 erneut zu durchsuchen.
- Ob Google intern gesetzte `nofollow` heute noch irgendeine Wirkung haben, ist ungeprüft. Die alte Praxis des „PageRank Sculpting" gilt seit Jahren als tot, eine aktuelle Google-Aussage dazu habe ich nicht gesucht.
- Wie interne Verlinkung die Auswahl von Quellen in AI Overviews beeinflusst — gehört zu Hebel 10.
