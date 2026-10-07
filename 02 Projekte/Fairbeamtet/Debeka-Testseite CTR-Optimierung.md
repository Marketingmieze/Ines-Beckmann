---
tags: [fairbeamtet, seo, ctr]
status: aktiv
erstellt: 2026-10-07
---

# Debeka-Testseite CTR-Optimierung

Umsetzung von [[04 Ressourcen/Googles No. 1/2026-10-07 - Schlachtplan Google Nr 1 - Debeka-Testseite - Fassung 2.pdf|Schlachtplan Google Nr. 1 – Fassung 2]]. Dieses Projekt begleitet Schritt 0–7 aus Abschnitt D des Plans mit konkreten, ausgefüllten Ergebnissen.

**Wichtig:** Laut Plan ist der Status "Plan, keine Aufgaben angelegt" – die 7 Entscheidungen aus Abschnitt H (z. B. Reihenfolge der Gruppen, Freigabe der Title-Entwürfe) sind noch offen und müssen von Sven getroffen werden, bevor an Title/Description tatsächlich etwas geändert wird. Schritt 0 unten braucht diese Freigabe noch nicht – es ist reine Beobachtung, keine Änderung.

## Schritt 0 — Prüfen, was Google überhaupt anzeigt

Ziel: Vor jeder Änderung sehen, was aktuell wirklich im Suchergebnis steht. Zwei Teile, beide von Hand bei Google, nicht im Tool.

### Teil 1 — Angezeigter Title vs. echter `<title>`-Tag

Zielseite laut Plan (ermittelt aus [[02 Projekte/Fairbeamtet/SEO-GEO Status Report.md|SEO-GEO Status Report]], finale URL nach den Redirect-Hops):
`fairbeamtet.de/debeka-private-krankenversicherung-beamte-test/`

Vorgehen je Zeile: `site:fairbeamtet.de/debeka-private-krankenversicherung-beamte-test/` bei Google eingeben, angezeigten Title abschreiben. Dann den echten `<title>`-Tag der Seite auslesen (Seitenquelltext oder SEO-Plugin) und daneben eintragen.

| Zielseite / Sprungmarke | Angezeigter Title bei Google | Echter `<title>`-Tag | Weicht ab? |
|---|---|---|---|
| Hauptseite (debeka-private-krankenversicherung-beamte-test) | Debeka Private Krankenversicherung für Beamte im Test | Debeka Private Krankenversicherung für Beamte im Test 2026 | **Ja – Google schneidet "2026" am Ende weg** |
| Anker 1 – #passt-die-debeka-zu-dir-so-findest-du-es-raus (2.107 Impr. / 0 Klicks / Pos. 7,48) | teilt sich <title> mit Hauptseite | Debeka Private Krankenversicherung für Beamte im Test 2026 | – |
| Anker 2 – #debeka-tarife-leistungen-im-detail (2.092 Impr. / 0 Klicks / Pos. 7,45) | teilt sich <title> mit Hauptseite | Debeka Private Krankenversicherung für Beamte im Test 2026 | – |
| Anker 3 – #debeka-pkv-fur-beamte-im-grossen-vergleich-2025-leistungen-kritik-alternativen (1.958 Impr. / 0 Klicks / Pos. 7,48) | teilt sich <title> mit Hauptseite | Debeka Private Krankenversicherung für Beamte im Test 2026 | **Anker-Slug sagt "2025", Überschrift auf der Seite sagt "2026" – Sprungmarke wurde beim letzten Update nicht angepasst** |
| Anker 4 – #wie-gut-ist-die-debeka-private-krankenversicherungwirklich-fur-beamte (1.878 Impr. / 0 Klicks / Pos. 7,50) | teilt sich <title> mit Hauptseite | Debeka Private Krankenversicherung für Beamte im Test 2026 | – |
| Anker 5 – #debeka-vs-andere-pkv-anbieter-wer-ist-besser-fur-beamte (1.773 Impr. / 0 Klicks / Pos. 7,49) | teilt sich <title> mit Hauptseite | Debeka Private Krankenversicherung für Beamte im Test 2026 | – |
| Anker 6 – #kritik-an-der-debeka-das-solltest-du-wissen (1.485 Impr. / 0 Klicks / Pos. 7,56) | teilt sich <title> mit Hauptseite | Debeka Private Krankenversicherung für Beamte im Test 2026 | – |

Summe: 11.293 Impressionen, 0 Klicks – stimmt exakt mit Abschnitt A im Schlachtplan überein. Abgerufen direkt aus der Google Search Console (über SEO Gets), nicht manuell nachgeschaut. Alle sechs Anker zeigen denselben `<title>`-Tag wie die Hauptseite, weil es technisch dieselbe HTML-Seite ist – nur mit Sprungmarke.

### Teil 2 — Die 5 größten Zero-Click-Anfragen in der echten Ergebnisliste

Aus Schritt 3 des Plans (Tabelle Seite 5) – das sind die fünf Anfragen mit 0 Klicks trotz Impressionen:

| Anfrage | Impr. / Pos. (laut Plan) | Was steht über uns? | Läuft ein KI-Block? | Wie sieht unser Snippet dort aus? | Welches Versprechen machen die Nachbarn? |
|---|---|---|---|---|---|
| tarif b30 debeka | 523 / 6,3 | Erst riesiger KI-Kasten, dann offizielle Debeka-Seite, dann Konkurrenz beamten-pkv-vergleichen.de | Ja, großer "Übersicht mit KI"-Kasten mit 5 Stichpunkten. Finanztip/Debeka/Thomas Schösser zitiert bei den ersten 4, **fairbeamtet.de nur beim letzten Punkt (Beitragsrückerstattung/BRE)** – also dabei, aber ganz am Ende, nicht bei den prominenten Punkten oben | Unser organisches Ergebnis ganz unten, nach mehreren anderen Ergebnissen, praktisch nur nach Scrollen sichtbar | Finanztip/Debeka: Vertragsgrundlagen & Tarifdetails direkt von der Quelle; beamten-pkv-vergleichen.de: "Debeka PKV Beamte: Bekannt heißt passend?" |
| debeka tarif bc leistungen | 642 / 9,9 | KI-Kasten, dann "Weitere Fragen" + Werbe-Kasten, dann Platz 1 beamtenservice.de, Platz 2 wir | Ja, zitiert Debeka, OPTINVEST Beamte, Lukas Mehlhardt – fairbeamtet.de NICHT zitiert | Platz 2, direkt sichtbar (besser als bei b30), Sterne 4,9★ (1.114) weiterhin sichtbar | beamtenservice.de: "Debeka Beihilfeergänzungstarif" |
| debeka tarif b20k | 286 / 6,7 | *(ausfüllen)* | *(ja/nein)* | *(ausfüllen)* | *(ausfüllen)* |
| debeka zahnersatz beamte | 364 / 8,6 | *(ausfüllen)* | *(ja/nein)* | *(ausfüllen)* | *(ausfüllen)* |
| debeka pkv tarife | 255 / 8,8 | *(ausfüllen)* | *(ja/nein)* | *(ausfüllen)* | *(ausfüllen)* |

### Beobachtungen unterwegs

- **07.10.2026:** Im echten Google-Ergebnis für die Hauptseite sind trotz Plan-Aussage (C2: Sterne "nicht zulässig") **weiterhin Sterne sichtbar** (4,9 ★★★★★, 1.114 Bewertungen). Widerspricht der Annahme im Schlachtplan, dass die Google-Berechtigung dafür fehlt – entweder zeigt Google sie trotzdem (Altbestand, Caching) oder die Einschätzung im Plan muss geprüft werden. Relevant für Entscheidung #5 (Sven).
- **07.10.2026:** Google schneidet die Jahreszahl "2026" am Ende des Titles ab (Tag: "...im Test 2026", angezeigt: "...im Test"). Bestätigt die Umschreibe-Tendenz aus C3 konkret für diese Seite. Relevant für Entscheidung #6 (Sven: Jahreszahlen pflegen oder streichen?).

### Ergebnis Schritt 0 (Fazit nach dem Ausfüllen)

*(Kurz zusammenfassen: Schreibt Google tatsächlich um? Was steht typischerweise über unserem Ergebnis? Daraus ergibt sich, worauf Schritt 2–4 besonders achten müssen.)*

## Nächste Schritte (noch nicht gestartet)

- [ ] Schritt 0 ausfüllen (oben)
- [ ] Schritt 1 – Zielanfrage je Seite festlegen
- [ ] Schritt 2 – Title nach Bauplan schreiben
- [ ] Schritt 3 – Entwürfe von Sven freigeben lassen
- [ ] Schritt 4 – Description schreiben
- [ ] Schritt 5 – H1 angleichen
- [ ] Schritt 6 – Anker-Entscheidung (abhängig von Svens Entscheidung #3)
- [ ] Schritt 7 – Messen ab erstem Monatswechsel nach Umsetzung

## Offene Entscheidungen von Sven (Abschnitt H im Plan)

1. Ebene 1 zuerst und allein – ja oder nein?
2. Reihenfolge der Gruppen: PKV-Lexikon (+326) vor Test > Gesellschaften (+281)?
3. Anker: eigene Antwortsätze oder aus dem Inhaltsverzeichnis entfernen?
4. Welche Erfahrungszahl ist belegbar: 6.000 oder 20.000?
5. Darf das Sterne-Widget die Schema-Auszeichnung verlieren?
6. Jahreszahlen in Titeln: pflegen oder streichen?
7. Priorität je Schritt
