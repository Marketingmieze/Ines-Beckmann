---
tags: [projekt, fairbeamtet, seo-geo, technik]
status: aktiv
erstellt: 2026-09-30
---

# Technischer SEO-Fix: Redirect-Ketten und 404-Fehler

> [!info] Kontext
> Vollständiger URL-Audit von fairbeamtet.de im Rahmen der Ursachenanalyse zum Traffic-Rückgang (siehe [[02 Projekte/Fairbeamtet/SEO-GEO Status Report.md|SEO-GEO Status Report]]). Geprüft wurden 662 eindeutige Content-URLs aus dem GSC-Pfadindex (via SEO Gets). Ergebnis: Duplicate Content durch die Migrationen ist **kein** Problem (alle alten URLs leiten korrekt weiter), aber es gibt zwei konkrete, fixbare Probleme: Redirect-Ketten und 404-Fehler. Die Seite läuft auf WordPress mit dem **Rank Math SEO Plugin** (erkennbar an der Sitemap-Struktur) – Rank Math hat ein eingebautes Redirections-Modul, das für alle Fixes unten ausreicht, ohne Code anzufassen.

## Zusammenfassung

| Problem | Anzahl | Schweregrad | Aufwand |
|---|---|---|---|
| Redirect-Ketten (2–3 Hops) | 42 | niedrig-mittel | klein (Bulk-Fix in Rank Math) |
| 404-Fehler bei plausiblen Tippfehlern/Altlasten | 22 | niedrig-mittel | klein-mittel |
| 404-Fehler durch vermutete KI-Halluzinationen (familienzuschlag-Cluster) | 36 | mittel (betrifft GEO/AI-Sichtbarkeit) | klein (1 Regel statt 36 Redirects) |

**Wichtig zur Einordnung:** Keines dieser Probleme erklärt allein den großen Traffic-Rückgang (siehe Status Report – die Hauptursache bleibt die Google-Update-Korrelation). Das hier ist Grundhygiene, die sich unabhängig davon lohnt: bessere Crawl-Effizienz, kein verschenktes Linkjuice, sauberere Nutzererfahrung bei Tippfehlern.

---

## Problem 1: Redirect-Ketten (42 Stück)

**Was ist das?** Eine URL leitet nicht direkt auf die finale Seite weiter, sondern über eine oder zwei Zwischenstationen (jede Station ein weiterer 301-Redirect). Das passiert typischerweise, wenn eine Website mehrfach umstrukturiert wird (hier: erst Kategorie-Präfixe wie `/pkv/`, `/beihilfe/`, `/bu-du/`, `/category/...` eingeführt, dann beim Relaunch am 16.01.2026 wieder auf flache URLs umgestellt) und die Redirects dabei nicht direkt auf das neue Endziel gesetzt, sondern nur auf die jeweils vorherige Zwischen-URL.

**Warum ist das ein Problem?**
- Jeder zusätzliche Hop kostet Crawl-Budget (Googlebot muss mehrfach nachfassen statt direkt zu landen)
- Etwas Linkkraft geht bei jedem Hop verloren
- Ladezeit für Nutzer, die über alte Links/Lesezeichen kommen, verschlechtert sich minimal
- Manche Tools/Bots brechen Ketten ab einer bestimmten Länge ab

**Wie löse ich das?**
1. In WordPress ins Rank Math-Menü gehen: **Rank Math → Redirections**
2. Für jede Zeile unten in der Tabelle: die bestehende Redirect-Regel für die Quell-URL (linke Spalte) suchen und ihr Ziel direkt auf die **letzte** URL der Kette ändern (rechte Spalte, letzter Eintrag) – die Zwischenstationen kannst du so überspringen
3. Falls für die Quell-URL noch keine explizite Regel in Rank Math existiert (sondern die Kette z. B. durch alte `.htaccess`-Einträge oder eine automatische WordPress-Slug-History entsteht), lege eine neue 301-Regel mit „Exact match" auf die Quelle und dem finalen Ziel als Redirect-URL an
4. Nach dem Speichern kurz mit einem Redirect-Checker (z. B. `httpstatus.io` oder Browser-Entwicklertools → Netzwerk-Tab) verifizieren, dass jetzt nur noch 1 Hop passiert

**Alle 42 Ketten** (Quelle → Zwischenstation(en) → finales Ziel):

| Quelle | Weg zum finalen Ziel |
|---|---|
| `/beihilfe-ratgeber/bemessungssaetze/` | `/beihilfe-ratgeber/beihilfe-bemessungssaetze` → `/beihilfe-ratgeber/beihilfe-bemessungssaetze/` |
| `/beihilfe/baden-wuerttemberg/` | `/beihilfe-baden-wuerttemberg` → `/beihilfe-baden-wuerttemberg/` |
| `/beihilfe/beihilfe-auf-einen-blick/baden-wuerttemberg/` | `/beihilfe-baden-wuerttemberg` → `/beihilfe-baden-wuerttemberg/` |
| `/beihilfe/beihilfe-baden-wuerttemberg-2023/` | `/beihilfe-baden-wuerttemberg` → `/beihilfe-baden-wuerttemberg/` |
| `/beihilfe/beihilfe-bund-laender/beihilfe-bw/` | `/beihilfe-baden-wuerttemberg` → `/beihilfe-baden-wuerttemberg/` |
| `/beihilfe/beihilfeaenderung-baden-wuerttemberg-2023/` | `/beihilfe-baden-wuerttemberg` → `/beihilfe-baden-wuerttemberg/` |
| `/beihilfe/bemessungssaetze-bund-laender/` | `/beihilfe-ratgeber/beihilfe-bemessungssaetze` → `/beihilfe-ratgeber/beihilfe-bemessungssaetze/` |
| `/beihilfe/hamburger-modell-pauschale-beihilfe/` | `/beihilfe-ratgeber/pauschale-beihilfe/` → `/pauschale-beihilfe/` |
| `/beihilfe/uebersicht-bundeslaender-beihilfe-app/` | `/app-bund-laender/` → `/beihilfe-ratgeber/beihilfe-apps/` |
| `/bu-du/7-gravierende-denkfehler-bu-du/` | `/bu-du-ratgeber/bu-du-denkfehler/` → `/bu-du-denkfehler/` |
| `/bu-du/beamte-dienstunfaehigkeit-sinnvoll/` | `/bu-du-ratgeber/dienstunfaehigkeitsversicherung-beamte-sinnvoll/` → `/dienstunfaehigkeitsversicherung-beamte-sinnvoll/` |
| `/bu-du/bu-oder-du-fuer-beamte-was-ist-besser/` | `/bu-du-ratgeber/dienst-oder-berufsunfaehigkeitsversicherung/` → `/dienst-oder-berufsunfaehigkeitsversicherung/` |
| `/bu-du/debeka-dienstunfaehigkeitsversicherung/` | `/bu-du-ratgeber/debeka-dienstunfaehigkeitsversicherung/` → `/debeka-dienstunfaehigkeitsversicherung/` |
| `/bu-du/du-beamte-sinnvoll-dienstunfaehigkeit/` | `/bu-du-ratgeber/dienstunfaehigkeitsversicherung-beamte-sinnvoll/` → `/dienstunfaehigkeitsversicherung-beamte-sinnvoll/` |
| `/bu-du/du-klassich-2-phasen-modell-ansparung/` | `/bu-du-ratgeber/du-abschlussmodelle/` → `/du-abschlussmodelle/` |
| `/bu-du/gefaehrliche-hobbys/` | `/bu-du-ratgeber/gefaehrliche-hobbys/` → `/gefaehrliche-hobbys/` |
| `/bu-du/krankheit-oder-hobby-nachmelden/` | `/bu-du-ratgeber/nachmeldepflicht/` → `/nachmeldepflicht/` |
| `/bu-du/rechtsschutzversicherung-berufunfaehigkeitsversicherung/` | `/bu-du-ratgeber/bu-rechtsschutz/` → `/bu-rechtsschutz/` |
| `/bu-du/sonderklauseln-du-versicherung/` | `/bu-du-ratgeber/sonderklauseln-du-versicherung/` → `/sonderklauseln-du-versicherung/` |
| `/bu-du/unfallversicherung-trotz-bu/` | `/bu-du-ratgeber/bu-unfallversicherung/` → `/bu-unfallversicherung/` |
| `/bu-du/vorvertragliche-anzeigenpflichtverletzung/` | `/bu-du-ratgeber/vorvertragliche-anzeigepflicht/` → `/vorvertragliche-anzeigepflicht/` |
| `/category/beihilfe-ratgeber/ambulante-leistungen/` | `/beihilfe-ratgeber/ambulante-leistungen/` → `/beihilfe-ratgeber/ambulante-leistungen-beihilfe/` |
| `/category/beihilfe-ratgeber/bemessungssaetze/` | `/beihilfe-ratgeber/bemessungssaetze/` → `/beihilfe-ratgeber/beihilfe-bemessungssaetze` → `/beihilfe-ratgeber/beihilfe-bemessungssaetze/` |
| `/category/beihilfe/` | `/beihilfe/` → `/beihilfe-ratgeber/beihilfe-bund-laender/` |
| `/category/bu-du-ratgeber/` | `/bu-du-ratgeber/` → `/berufsunfaehigkeitsversicherung/` |
| `/category/bu-du/` | `/bu-du/` → `/bu-du-denkfehler/` |
| `/category/lp/` | `/lp/` → `/dienstunfaehigkeitsversicherung/lp-berufs-und-dienstunfaehigkeitsversicherung/` → `/berufsunfaehigkeitsversicherung/` |
| `/category/pkv-ratgeber/` | `/pkv-ratgeber/` → `/private-krankenversicherung/` |
| `/category/pkv-ratgeber/pkv-lexikon/` | `/pkv-ratgeber/pkv-lexikon/` → `/pkv-ratgeber/private-krankenversicherung-lexikon-beamte` → `/pkv-ratgeber/private-krankenversicherung-lexikon-beamte/` |
| `/category/pkv-ratgeber/pkv-tipps-tricks/` | `/pkv-ratgeber/pkv-tipps-tricks/` → `/private-krankenversicherung/` |
| `/category/pkv-ratgeber/test-pkv-beamte/` | `/pkv-ratgeber/test-pkv-beamte/` → `/pkv-ratgeber/private-krankenversicherung-beamte-test/` |
| `/category/pkv/` | `/pkv/` → `/private-krankenversicherung/` |
| `/category/pkv/page/3/` | `/pkv/page/3/` → `/youtube/pkv-beamte-beratungsvideo-sven/` |
| `/category/pkv/page/4/` | `/pkv/page/4/` → `/youtube/pkv-beamte-beratungsvideo-sven/` |
| `/category/unser-team/` | `/unser-team/` → `/mitarbeiter/` → `/geschaeftsfuehrung-und-mitarbeiter/` |
| `/category/unser-team/mitarbeiter/` | `/unser-team/mitarbeiter/` → `/geschaeftsfuehrung-und-mitarbeiter/` |
| `/debeka-krankenversicherung-beamte-test-2025/` | `/private-krankenversicherung/gesellschaften/debeka/` → `/debeka-private-krankenversicherung-beamte-test/` |
| `/lp/berufs-und-dienstunfaehigkeitsversicherung-1/` | `/dienstunfaehigkeitsversicherung/lp-berufs-und-dienstunfaehigkeitsversicherung/` → `/berufsunfaehigkeitsversicherung/` |
| `/lp/berufsunfaehigkeitsversicherung-fuer-lehrer/` | `/dienstunfaehigkeitsversicherung/lp-berufs-und-dienstunfaehigkeitsversicherung/` → `/berufsunfaehigkeitsversicherung/` |
| `/pkv-ratgeber/pkv-lexikon/` | `/pkv-ratgeber/private-krankenversicherung-lexikon-beamte` → `/pkv-ratgeber/private-krankenversicherung-lexikon-beamte/` |
| `/pkv/private-krankenversicherung-debeka/` | `/private-krankenversicherung/gesellschaften/debeka/` → `/debeka-private-krankenversicherung-beamte-test/` |
| `/unser-team-fairbeamtet/` | `/mitarbeiter/` → `/geschaeftsfuehrung-und-mitarbeiter/` |

**Zusatzbeobachtung:** Mehrere Ketten laufen über dieselben Zwischenstationen (z. B. alles rund um `/beihilfe-baden-wuerttemberg/`, `/bu-du-ratgeber/...`, `/pkv-ratgeber/...`). Wenn du in Rank Math nach diesen Zwischen-URLs suchst, kannst du oft mehrere Ketten in einem Rutsch fixen, indem du die Regel für die Zwischen-URL direkt auf das Endziel umbiegst – dann korrigieren sich alle Quellen, die über sie laufen, automatisch mit.

---

## Problem 2: 404-Fehler bei plausiblen Tippfehlern/Altlasten (22 Stück)

**Was ist das?** URLs, die im GSC-Pfadindex auftauchen (also irgendwann einmal gecrawlt oder verlinkt wurden), aber aktuell einen echten 404-Fehler ohne jeden Redirect liefern. Für die meisten ist ein plausibles Ziel erkennbar (Tippfehler-Variante, alte Autoren-/Produktbezeichnung, URL-kodierte Umlaut-Version).

**Warum ist das ein Problem?** Nutzer und Suchmaschinen, die über alte Links, Lesezeichen oder (bei den Umlaut-Versionen) über kopierte URLs mit Sonderzeichen kommen, landen auf einer Fehlerseite statt auf Content. Das ist schlechte Nutzererfahrung und verschenktes Linkjuice, falls diese URLs noch irgendwo extern verlinkt sind.

**Wie löse ich das?** Für jede Zeile: in **Rank Math → Redirections → Add New**, Quelle exakt eintragen (inkl. Slash am Ende, so wie in der Tabelle), Ziel eintragen, Typ „301 – Permanent Move". Bei den mit „manuell prüfen" markierten Zeilen erst kurz schauen, ob der Inhalt tatsächlich noch existiert oder bewusst entfernt wurde, bevor du redirectest.

| 404-URL | Vermutetes Ziel | Sicherheit |
|---|---|---|
| `/amts%C3%A4rztliche-untersuchung/` | `/amtsaerztliche-untersuchung/` | sicher (URL-kodierte Umlaut-Version derselben Seite) |
| `/zahn%C3%A4rztliche-leistungen-beihilfe-berlin/` | `/zahnaerztliche-leistungen-beihilfe-berlin/` | sicher (URL-kodierte Umlaut-Version) |
| `/dienstunf%C3%A4higkeitsversicherung-beamte/` | `/dienstunfaehigkeitsversicherung-beamte/` | sicher (URL-kodierte Umlaut-Version) |
| `/beamte-kinder-gkv-ok-pkv-versichern/` | `/beamte-kinder-gkv-oder-pkv-versichern/` | sicher (Tippfehler „ok" statt „oder") |
| `/kindergeld-fuer-bien-beamte/` | `/kindergeld-fuer-beamte/` | sicher (Tippfehler „bien") |
| `/debeka-oder-debeka-pkv-beamte-vergleich/` | `/debeka-oder-dbv-pkv-beamte-vergleich/` | sicher (Tippfehler, „debeka" statt „dbv") |
| `/debeka-or-dbv-pkv-beamte-vergleich/` | `/debeka-oder-dbv-pkv-beamte-vergleich/` | sicher (Tippfehler „or" statt „oder") |
| `/berufsunfaehigkeit-cannabis/` | `/berufsunfaehigkeitsversicherung-cannabis/` | wahrscheinlich (gekürzte Variante) |
| `/luisa-pkv-expertin-fairbeamtet/` | `/luisa-bensmaya-pkv-expertin-fairbeamtet/` | wahrscheinlich (Nachname fehlt) |
| `/private-krankenversicherung-mit-heuschnupfen-risikozuschlag/` | `/private-krankenversicherung-mit-heuschnupfen/` | wahrscheinlich |
| `/dienstunfaehigkeit-polizei/` | `/dienstunfaehigkeitsversicherung-polizei/` | wahrscheinlich |
| `/dienstunfaehigkeitsversicherung/polizei/` | `/dienstunfaehigkeitsversicherung-polizei/` | wahrscheinlich |
| `/amtsaerztliche-begutachtung/` | `/amtsaerztliche-untersuchung/` | wahrscheinlich (Synonym) |
| `/angst-vor-dem-amtsarzt-was-tun-der-amtsarzt-verweigert-die-bescheinigung/` | `/amtsaerztliche-untersuchung/` | wahrscheinlich (thematisch verwandt, ggf. alter Unterabschnitt) |
| `/katalog-kindergeld-fuer-beamte/` | `/kindergeld-fuer-beamte/` | wahrscheinlich |
| `/freunde-empfehlen-freunde/` | `/pkv-empfehlung-freunde-kollegen/` | wahrscheinlich |
| `/pkv/beitragsanpassung-debeka-2025-pkv-erhoehung/` | `/debeka-beitragserhoehung-2025/` | wahrscheinlich |
| `/pkv/private-krankenversicherung-beamte-anwaerter/` | `/private-krankenversicherung/beamtenanwaerter/` | wahrscheinlich |
| `/private-krankenversicherung-beamtenanwaerter/` | `/private-krankenversicherung/beamtenanwaerter/` | wahrscheinlich |
| `/dienstunfaehigkeitsversicherung-lehrer-2026/` | – | manuell prüfen (evtl. geplanter, noch nicht veröffentlichter Artikel statt Altlast) |
| `/private-krankenversicherung/bmi-ergebnis/` | – | manuell prüfen (klingt nach dynamischer Tool-Ergebnisseite, kein normaler Artikel) |
| `/simplr-app-digitaler-versicherungsmanager/` | – | manuell prüfen (evtl. bewusst entfernter Kooperationsartikel – dann eher 410 „Gone" statt Redirect) |

---

## Problem 3: 404-Cluster „familienzuschlag" – vermutlich KI-Crawler/Zitat-Traffic (36 Stück)

**Was ist das?** 36 der 58 gefundenen 404-Fehler sind Varianten des Themas „Familienzuschlag" – der mit Abstand traffic-stärksten Seite der ganzen Domain (`/familienzuschlag-fuer-beamte/`, 2.084 Klicks/95.861 Impressions allein im September, siehe Status Report). Die Varianten sind auffällig „hallucination-artig": Tippfehler wie `/familienzuschlag-fuer-baemte/`, `/familienzuschuer-fuer-beamte/`, unsinnige Kombinationen wie `/familienzuschlag-fuer-familienzuschlag/`, `/familienzuschlag-fuer-fairbeamtet/`, `/familienzuschlag-fuer-ein-beamter/`, sogar ein Stern im Slug (`/familienzuschlag-fuer-beamt*en/`).

**Warum vermutlich KI-Crawler/Zitate?** fairbeamtet.de wird laut Status Report bereits mit 271 KI-Zitaten aktiv von LLM-Systemen (GEO) referenziert. Wenn ein KI-System (ChatGPT, Perplexity, Google AI Overviews o. ä.) beim Zusammenfassen oder Zitieren des Artikels die URL leicht falsch wiedergibt oder „erfindet" – ein bekanntes Phänomen bei LLM-generierten Links – und Nutzer diesen Links folgen (oder andere Crawler sie prüfen), entstehen genau solche Fehlerhäufungen um das populärste Thema der Seite. Das ist eine Hypothese, keine bewiesene Ursache (die Serverlogs würden das zeigen, GSC/Ahrefs geben das nicht her), aber das Muster (fast nur beim traffic-stärksten Artikel, viele leicht-daneben-Varianten, teils mit für Menschen untypischen Fehlern wie dem Sternchen) passt gut dazu.

**Warum lohnt sich der Fix trotzdem, unabhängig von der genauen Ursache?** Jeder Nutzer oder Bot, der über eine dieser Varianten kommt, landet auf einer 404-Seite statt auf dem Artikel – bei einem derart zentralen Thema ist das ärgerlich viel verschenkter Traffic bzw. eine schlechte Erfahrung für alle, die über KI-Suchsysteme auf die Seite finden.

**Wie löse ich das – effizient statt 36 Einzel-Redirects?**

Rank Math unterstützt **Regex-Matching** bei Redirects. Statt 36 einzelne Regeln anzulegen, reicht eine einzige Regel:

1. **Rank Math → Redirections → Add New**
2. Match-Typ auf **„Regex"** stellen
3. Als Quelle: `^/familienzuschlag.*$` bzw. genauer `^/familienzuschl(a|ä)(g|ge|f|ue|uer).*$` um auch Varianten wie „familienzuschuer" abzudecken – am einfachsten ist ein breiter Catch-all: `^/familienzuschl.*` und `^/familienzusch(u|ue)er.*`
4. **Wichtig:** Die echte Zielseite `/familienzuschlag-fuer-beamte/` selbst muss von der Regel ausgeschlossen bleiben, sonst redirected sie auf sich selbst (Rank Math prüft meist automatisch exakte Treffer zuerst, zur Sicherheit trotzdem testen)
5. Ziel: `/familienzuschlag-fuer-beamte/`
6. Typ: 301
7. Speichern und mit 2–3 der URLs aus der Liste unten testen (z. B. `fairbeamtet.de/familienzuschlag-fuer-baemte/` im Browser aufrufen, sollte jetzt auf den echten Artikel weiterleiten)

Betroffene 404-URLs (zur Kontrolle/zum Testen):

`/familienzuschlaege-fuer-beamte`, `/familienzuschlaf-fuer-beamte/`, `/familienzuschlag-einfach-erklaert/`, `/familienzuschlag-for-beamte/`, `/familienzuschlag-fuer-badge-anspruch-2026/`, `/familienzuschlag-fuer-badge/`, `/familienzuschlag-fuer-baemte/`, `/familienzuschlag-fuer-bayern`, `/familienzuschlag-fuer-bayern/`, `/familienzuschlag-fuer-beamt*en/`, `/familienzuschlag-fuer-beamte-hoehe-anspruch/`, `/familienzuschlag-fuer-beamte-hoehe-und-anspruch-2026`, `/familienzuschlag-fuer-beamte-hoehe-und-anspruch-2026/`, `/familienzuschlag-fuer-beamte/hoehe-und-anspruch-2026`, `/familienzuschlag-fuer-beamten/`, `/familienzuschlag-fuer-beamteten-anspruch-stufen-hoehe`, `/familienzuschlag-fuer-beamtin`, `/familienzuschlag-fuer-beamtin-und-beamte/`, `/familienzuschlag-fuer-beamtin/`, `/familienzuschlag-fuer-beamtinnen-und-beamte-anspruch-stufen-hoehe`, `/familienzuschlag-fuer-beamtinnen-und-beamte/`, `/familienzuschlag-fuer-bebten/`, `/familienzuschlag-fuer-beratende/`, `/familienzuschlag-fuer-beratenden/`, `/familienzuschlag-fuer-bewebeamte/`, `/familienzuschlag-fuer-bienbeamte/`, `/familienzuschlag-fuer-bund/`, `/familienzuschlag-fuer-bundesbeamte/`, `/familienzuschlag-fuer-ein-beamter/`, `/familienzuschlag-fuer-fairbeamtet/`, `/familienzuschlag-fuer-familien/`, `/familienzuschlag-fuer-familienzuschlag/`, `/familienzuschlag-fuer-haben-beamte-2026`, `/familienzuschlag-fuer-teilzeit/`, `/familienzuschlag-hoehe-und-anspruch-2026/`, `/familienzuschuer-fuer-beamte/`

**Alternative ohne Regex** (falls Rank Math in eurer Version/Lizenz kein Regex unterstützt): Die Redirects-Match-Art „Contains" nutzen, Quelle `familienzuschlag` (oder `familienzusch`), Ziel `/familienzuschlag-fuer-beamte/` – funktioniert in den meisten Rank Math-Versionen genauso als Catch-all.

---

## Empfohlene Reihenfolge

1. **Problem 3 zuerst** (eine Regel, größter Hebel, betrifft das wichtigste Thema der Seite)
2. **Problem 2** (22 Einzel-Redirects, aber die „sicheren" zuerst, die 3 „manuell prüfen"-Fälle zuletzt und mit Sven abklären)
3. **Problem 1** (42 Ketten – niedrigste Priorität, da schon funktionierende Redirects, nur Optimierung; am besten über die gemeinsamen Zwischenstationen bündeln, siehe Zusatzbeobachtung oben)

## Offene Punkte

- Ursache der familienzuschlag-404-Häufung ist eine Hypothese (KI-Zitat-Halluzination), nicht bewiesen. Bei Zugriff auf die Server-Logs (z. B. über den Hosting-Provider) ließe sich anhand der User-Agents prüfen, ob die Anfragen tatsächlich von bekannten KI-Crawlern/Referrern kommen.
- Die drei „manuell prüfen"-Fälle in Problem 2 sollten vor dem Redirect kurz mit Sven abgestimmt werden (könnten absichtlich entfernte Inhalte sein).
