---
tags: [ressource, ahrefs, seo]
erstellt: 2026-10-28
---

# Organic Pages by Type (Ahrefs Site Explorer)

## Was es ist

Neues Feature in Ahrefs, released September 2026, Teil der [[04 Ressourcen/Ahrefs/Ahrefs|Ahrefs]]-Updates. Ankündigung per Mail von Ahrefs (28.10.2026, Betreff "Sept '26 product updates: AI Discoverability, Page types, and more") und im zugehörigen YouTube-Video: [Ahrefs September 2026 Product Updates](https://www.youtube.com/watch?v=oWrVGjks_cI).

Das neue Widget **"Organic pages by type"** in der Site Explorer Overview schlüsselt auf, **welche Seiten-Typen** (z. B. Blog, Tools, Service-Seiten) einer Domain den organischen Traffic bringen.

## Warum relevant für uns

Direkt anwendbar für fairbeamtet.de-Analysen (siehe [[02 Projekte/Fairbeamtet/SEO-GEO Status Report.md|SEO-GEO Status Report]] und [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]]):

- **Eigene Seite analysieren**: Zeigt, welche Seiten-Typen auf fairbeamtet.de tatsächlich Traffic bringen (Ratgeber/Blog vs. Rechner/Tools vs. Landingpages vs. Service-Seiten) – nicht nur wie viele Seiten es pro Typ gibt.
- **Wettbewerber analysieren**: Auf Konkurrenz-Domains laufen lassen, um zu sehen, welche Content-Typen bei ihnen wirklich ziehen.
- **Ableitung für die Strategie**: Zeigt, welche Seiten-Typen man **mehr** produzieren müsste, um mehr Traffic zu generieren – statt wahllos neue Ratgeber zu schreiben, gezielt den Typ ausbauen, der bei uns oder der Konkurrenz am besten funktioniert.
- Klick auf einen Seiten-Typ im Widget springt direkt zum gefilterten Top-Pages-Report für diesen Typ.

## Nächster Schritt (Idee, noch nicht umgesetzt)

Wenn das Feature in unserem Ahrefs-Account verfügbar ist: Site Explorer → Overview von fairbeamtet.de und 2–3 Hauptwettbewerbern aufrufen, "Organic pages by type" auswerten und mit den Erkenntnissen die Content-Planung (Claudia-Workflow) abgleichen – welche Seiten-Typen sollten wir priorisieren?

## Weitere Updates aus dem gleichen Release (zur Vollständigkeit)

- **AI Discoverability** (Site Audit): neue Issue-Kategorie, prüft ob AI-Crawler (ChatGPT, Perplexity, Google AI) Seiten lesen/zitieren können (robots.txt-Blocks, zu langsame/schwere Seiten, inkonsistente Bot-Policies, JS-Rendering-Probleme).
- **Semantische Filter** (Keywords Explorer): Filtert Keyword-Listen nach Bedeutung statt exaktem Wortmatch – nützlich bei mehrdeutigen Begriffen.
- **Bot Analytics**: jetzt direkt verbindbar mit Vercel, Amazon CloudFront, Fastly.
- API-Unit-Limits auf allen Plänen verdoppelt, neue API v3 Endpoints (u. a. Top 1 Mio. Domains nach Domain Rating, Content Helper Topics API).

## Transkript des Videos (Volltext, automatisch generiert, EN)

> Hello and welcome to Ahrefs monthly product updates. I picked five updates we shipped in September that you cannot miss. Let's start with something big. More and more people will find brands through ChatGPT, Perplexity or Google's AI answers. But if AI bots can't crawl or read your pages, you won't get cited no matter how good your content is. That's why we built AI discoverability, a brand new issue category inside Site Audit. It checks how well your site can be crawled, read, and cited by AI search tools so you can catch these blockers in the audit you already run. The first batch of issues covers pages blocked by AI bots in robots.txt, pages too slow or heavy for AI crawlers, inconsistent AI bot policies and similar AI generated content. We also flag pages that need JavaScript rendering because most AI bots, including ChatGPT and Claude, can't really read it and we don't want your content to be invisible to them unless it's intentional. And there is a lot more coming, including all of these very, very soon.
>
> Next up is Site Explorer. Knowing how many pages a site has tells you very little. What matters is what pages bring in traffic because that tells you where to invest. The new organic pages by type widget in the overview shows exactly that. Take Ahrefs — the page is huge, but most of our traffic actually comes from service pages like our free tools. Run this on a competitor and you'll see what's really working for them so you can double down on the right types of content for your site.
>
> Now, let's move on to Keywords Explorer. Matching for the exact word can be really noisy. Say you're researching the running shoe brand On. Search for "on" and you'll get thousands of unrelated keywords because of the nature of the word. The new semantic filters fix that by matching meaning instead of just words. Add "running shoes" as a semantic filter and you'll get keywords like "oncloud running shoes" where "on" is the brand. This gives you much cleaner keyword lists and a lot less time spent filtering out irrelevant terms by hand.
>
> Next are Bot Analytics. Bot analytics shows you how search engines and AI crawlers actually move through your site. But you only get those insights if your logs are connected. If your site runs on Vercel, Amazon CloudFront or Fastly, this just got a lot easier. You can now connect all three directly under project settings → Bot Analytics.
>
> And my favorite update as last — we doubled API unit limits on all plans. The reason is quite simple: more and more of you are pulling Ahrefs data into AI assistants and automated workflows through our MCP or API. Doubling the limits means you can build and run those workflows without hitting the ceiling anytime soon. We also added a few new API v3 endpoints, including a public list of the top 1 million domains by domain rating, which is great for prospecting and benchmarking. There's also a new content helper topics API that scores how well your page covers the core topics of top ranking pages, so you can audit content at scale instead of page by page. Plus, there are a couple of API additions for managing projects and brand radar prompts. You'll find all of them in the changelog.
>
> And that's it for September. Head to our changelog for everything we shipped and send us your feature ideas on Canny. Your request could be in next month's video. See you later.

## Quellen

- E-Mail: "Sept '26 product updates: AI Discoverability, Page types, and more" (Ahrefs, 28.10.2026)
- Blogpost: [ahrefs.com/blog/new-features-september-2026](https://ahrefs.com/blog/new-features-september-2026/)
- Video: [youtube.com/watch?v=oWrVGjks_cI](https://www.youtube.com/watch?v=oWrVGjks_cI)
