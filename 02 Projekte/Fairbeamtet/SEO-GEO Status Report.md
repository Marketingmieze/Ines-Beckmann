---
tags: [projekt, fairbeamtet, status-report]
quelle: "Agenten-Report (Content-/SEO-Team von Sven Höhne), ungefähr Februar/März 2026"
überarbeitet: "Sprachlich überarbeitet nach [[04 Ressourcen/Schreibregeln/KI-Klang vermeiden - Fairbeamtet.md|KI-Klang vermeiden – Fairbeamtet]]"
---

# SEO-GEO Status Report

> [!info] Kontext
> Status-Report aus dem Agenten-gestützten Content-/SEO-System, das Sven für fairbeamtet.de nutzt (Agenten u. a. Günter, Rainer, Nils, Greta, Konrad, Axel, Gerd, Mia). Relevant für [[02 Projekte/Fairbeamtet/SEO-GEO-Optimierung.md|SEO-GEO-Optimierung]] und [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]].

## Wo wir stark sind

1. **Wir messen.** Das ist seltener, als man denkt. Die meisten Agenturen liefern Meinungen. Wir haben Search Console, Ahrefs, feste Growing-/Decaying-Schwellen, einen Monatsrhythmus und eine Protokollpflicht für jede Änderung. Ab heute kann niemand mehr behaupten, etwas habe gewirkt, ohne es zu zeigen.
2. **Belegkultur.** Die Playbooks führen Quellen mit Datum und Belegstufe. Heute hat Günter eine Zahl zurückgewiesen, Rainer hat eine kursierende Studie nicht verwendet, weil er die Methodik nicht fand, und Nils hat eine Analyse ausgeschlossen, weil sie als „Deleted"-Agenten markiert war. Das System korrigiert sich selbst. Das ist der eigentliche Wert.
3. **Compliance fährt mit.** Bei einem regulierten YMYL-Thema ist das der Grund, warum wir keinen Rückbau nach einer Abmahnung riskieren.
4. **Bekannte Fehler sind strukturell ausgeschlossen.** Keine Score-Ziele, keine Begriffsdichte, maximal 5 Vorschläge, „nichts anfassen, was funktioniert", eine Änderung dann messen.
5. **Die eigene KI-Position ist bekannt.** 271 Zitate, Platz 2 der Nische. Das wusste vor heute niemand, auch die Wettbewerber nicht.

## Wo wir schwach sind

| Schwäche | Wie schlimm |
|---|---|
| Null Output: die ganze Kette ist an echtem Content ungetestet | kritisch. Jede Annahme darin ist unbewiesen |
| Der Flaschenhals ist der Mensch: 23 Agenten helfen nicht, wenn der einzige Autor keine Zeit hat | kritisch. Bestimmt das echte Tempo |
| Leads sind blind: GA4 zählt nichts (Key Events = 0), die wichtigste Kennzahl wird von Hand gezählt | hoch |
| Kein Technik-Zuständiger für Indexhygiene und Core Web Vitals | hoch, aber ohne neuen Agenten lösbar |
| Kein Link- und PR-Zuständiger, obwohl Backlinks belegt wirksam sind | hoch |
| GEO ist dünner als das Etikett verspricht | mittel, siehe unten |

**Zu GEO:** Es gibt ein Playbook, additive Elemente werden gebaut, Zitate werden gemessen. Was fehlt, ist Entitäten-Arbeit: dass Google und die LLMs "fairbeamtet" und "Sven Höhne" als feste Größen mit klarem Themengebiet kennen, konsistente Angaben überall, Autorenprofile als echte Entitätsseiten, Erwähnungen außerhalb der eigenen Domain. Dafür ist aktuell niemand zuständig. Ohne das bleibt GEO Kosmetik am einzelnen Artikel.

## Was vergessen wurde

1. **Kundenanfragen.** Täglicher Kontakt mit Beamten, die Fragen stellen, die in keinem Tool auftauchen. Das ist echte Experience im Sinne von E-E-A-T: der einzige Rohstoff, den kein Wettbewerber kopieren kann. Dafür gibt es aktuell keinen Prozess. Das ist die größte vergessene Sache.
2. **Pflege statt Neubau.** Ein Aktualitätsregister für Beihilfesätze und Beiträge ist definiert, aber nicht aufgesetzt. Solcher Content veraltet von selbst.
3. **Bild und Video.** Kommt bei fairbeamtet.de aktuell nicht vor, obwohl es wichtige SERP-Flächen sind. (Anknüpfungspunkt: [[02 Projekte/Fairbeamtet/Social-Media-Start.md|Social-Media-Start]])
4. **BU/DU.** Bewusst zurückgestellt. Zweites Standbein, aktuell ohne Fachagenten.

## Was gebraucht wird, in dieser Reihenfolge

| # | Was | Wirkung/Aufwand | Begründung |
|---|---|---|---|
| 1 | 🍎 Einen Artikel komplett durch die Kette ziehen (kein neuer Agent, nur einmal ernst machen) | hoch/klein | Deckt alle Konstruktionsfehler auf einmal auf |
| 2 | 🍎 Lead-Messung reparieren (Fluent Forms → GA4 als Key Event) | hoch/klein | Ohne sie wird auf Traffic statt auf Geschäft optimiert |
| 3 | 🎯 Beratungsfälle erschließen: ein Ablauf, der echte Kundenfragen zu Content-Rohstoff macht | sehr hoch/mittel | Der einzige uneinholbare Vorsprung |
| 4 | 🎯 Technik-Audit (Indexhygiene, Core Web Vitals) | hoch/mittel | Kein neuer Agent nötig |
| 5 | 🎯 Entitäten und PR: ein Zuständiger für Markenbekanntheit und verdiente Links | hoch/groß | Erst wenn Artikel existieren, die verlinkt werden können |

**Bewusst weggelassen:** Neue Agenten für die restlichen Lücken. Es besteht ein Bau-Problem. Jeder weitere Agent vor dem ersten fertigen Artikel macht es schlimmer.

**🚫 Nicht machen:** Bestehende Seiten „auf Verdacht" überarbeiten. Es gibt jetzt Messung. Ab jetzt gilt: erst Befund, dann Hand anlegen.

## Wettbewerbsanalyse: Linkwachstum vs. Ranking-Erfolg

Größter Befund: Bei allen drei Mitbewerbern läuft das Linkwachstum gegenläufig zum Erfolg. Der einzige, der nicht eingebrochen ist, hat Links verloren.

| Wettbewerber | Backlinks (6 Mon.) | Verw. Domains | Top-3 | Verlauf |
|---|---|---|---|---|
| beamtenservice | −49% | −27% | −5% | stabil |
| beamtenberater | +153% | +260% | −60% | Absturz |
| Kuhlen | +95% | +147% | −49% | Absturz |

**Interpretation (mit Vorsicht):** Wahrscheinlichste Erklärung: Zwei Seiten sind gefallen und haben als Reaktion Links aufgebaut, vermutlich billige, in Masse. Es hat nicht geholfen. Konrad hat das als Korrelation bei n=3 gekennzeichnet, mit offener Nachforderung: Wie hoch ist der Spam-Anteil der neu hinzugekommenen Domains? Ist er hoch, erklärt das den Zusammenhang.

**Zweiter Befund:** Trust-Bausteine auf der Startseite erklären den Unterschied nicht. Beamtenberater hat 8 namentliche Berater, TÜV-Logo und 4,9 Sterne bei 127 Bewertungen. Kuhlen hat 319 ProvenExpert-Bewertungen. Beide sind trotzdem abgestürzt. Trust-Bausteine bleiben trotzdem richtig, weil sie für Leser und für YMYL-Qualität wichtig sind.

**Was beamtenservice, der stabile Wettbewerber, anders macht:** Die traffic-stärkste Seite ist eine eigene kritische Analyse: eine Testsieger-Historie 2022–2026 mit Methodik-Kritik an Handelsblatt und Stiftung Warentest. Der Verlierer daneben hat auf seiner Top-Seite eine Standard-Erklärung ohne Tabelle. Einschränkung: nur eine Seite je Domain geprüft, die Aussage steht auf dünner Basis. Ansatzpunkte für Verbesserung: sichtbares Aktualisierungsdatum statt nur im Fließtext, namentlicher Autor mit Registernummer (fehlt bei beamtenservice), Primärquellen statt Presseartikel.

**Ausdrücklich als „nicht machen" markiert:**
- 🚫 Kein Linkaufbau nach Zahl. Genau die zwei Domains mit dem stärksten Linkwachstum sind am tiefsten gefallen.
- 🚫 Presselogos und Bewertungssterne nachbauen. Korreliert hier nicht mit Erfolg, bei Sternen kommt zusätzlich ein Compliance-Vorbehalt dazu.

**Neue Messregel:** Künftige Monatschecks stützen sich auf Keywords und Top-3-Platzierungen statt auf Traffic-Schätzungen. Gezählte Positionen sind durch Ahrefs' Modellwechsel nicht verfälschbar, geschätzter Traffic schon.

## Offene Punkte

- Spam-Anteil der neu hinzugekommenen Wettbewerber-Domains wird noch geprüft.
- Offene Frage fürs Playbook: Soll die Beobachtung "Linkwachstum lief bei drei Domains gegenläufig zum Erfolg" (n=3, fehlende Spam-Prüfung) in Abschnitt 9.1 aufgenommen werden? Empfehlung: warten, bis die Spam-Zahlen vorliegen.
