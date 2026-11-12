---
tags: [projekt, marketingmieze]
status: aktiv
erstellt: 2026-09-23
---

# Website-Aufbau (marketingmieze.com)

## Ziel

Die eigene Website marketingmieze.com aufbauen – ein Mix aus persönlichem Blog und Wissensvermittlung im Bereich Marketing. Soll nicht "private Hirngrütze" sein, sondern anderen Menschen konkret etwas beibringen, das sie im Marketing anwenden können.

## Status

In Bearbeitung – Ideenfindung, Website noch nicht online.

## Nächste Schritte

- [x] Konkrete Themen-/Content-Ideen sammeln (persönlicher Blog-Winkel)
- [ ] Branding festlegen (Farben, Schrift, Logo)
- [ ] Erste Artikel-Idee ausformulieren und Feedback einholen

## Notizen

Schreibstil frecher und direkter als fairbeamtet.de, siehe [[00 Kontext/Marketingmieze/Schreibstil.md|Schreibstil]].

Geplantes Tool-Feature (eigenes Projekt): [[02 Projekte/Marketingmieze/BMI-Rechner.md|BMI-Rechner]].

## Kategorie-Struktur

Entscheidung 2026-11-12: Startseite zeigt drei Themenblöcke ("WordPress & Technik", "Social Media & Marketing", "Mein Leben"). Gesamtstruktur so geplant, dass sie sich mit den schon bestehenden Content-Plänen deckt (Rants-Serie, "worüber keiner redet"-Serie) statt künstlich neue Kategorien zu erfinden. Maximal zwei Ebenen, keine leeren Kategorien auf Vorrat.

**WordPress & Technik** (Slug `wordpress-technik`, bereits angelegt)
> Ich lerne WordPress gerade selbst, mitten im Chaos, mit allen Fehlern inklusive. Kein Tutorial von oben herab – du siehst zu, wie ich's mir selbst beibringe.

Keine Unterkategorie vorerst – erst aufsplitten, wenn sich zwei klar unterschiedliche Content-Typen zeigen (z. B. Lernprozess vs. echte Anleitungen).

**Social Media & Marketing** (Slug `social-media-marketing`)
> Kein Bullshit, keine Buzzword-Bingo-Strategien. Nur das, was ich im echten Job und auf eigene Faust ausprobiert hab – was funktioniert und was dir keiner sagt.

Unterkategorien:
- **Klartext** (Slug `klartext`) – die geplante Rants-Serie über unehrliche Marketing-Praktiken (Clickbait, Fake-Bewertungen, künstliche Verknappung, ungekennzeichneter KI-Content, siehe Content-Ideen oben)
  > Unehrliche Marketing-Tricks, einmal auseinandergenommen. Clickbait, Fake-Bewertungen, künstliche Verknappung – hier wird draufgezeigt, nicht mitgemacht.
- **Ausprobiert** (Slug `ausprobiert`) – eigene Erfahrungen, was im Marketing wirklich funktioniert
  > Kein Bullshit, keine Theorie aus dem Lehrbuch. Nur das, was ich selbst getestet hab – inklusive dem, was nicht funktioniert hat.

**Mein Leben** (Slug `mein-leben`)
> Kein WordPress. Kein Marketing. Nur mein Leben: Familie, Chaos, Körper, ein Kater, der sich für den Chef hält. Nichts davon hübsch inszeniert.

Unterkategorie:
- **Unverblümt** (Slug `unverbluemt` – WordPress wandelt ü automatisch in "ue" um) – deckt sowohl Gesundheitsthemen (wie den BMI-Rechner-Beitrag) als auch die geplante "worüber keiner redet"-Serie ab (Care-Arbeit, Erschöpfung, finanzielle Scham, Druck für alle da zu sein, Einsamkeit) – gleicher Ton, gleiches Versprechen, deshalb eine gemeinsame Kategorie statt zwei
  > Hier wird nichts schöngeredet. Gesundheit, Körper, Zeug, über das sonst keiner redet. Hier schon.

Leichtere Alltagsgeschichten (Sohn, Kater Moony, WordPress-Chaos-Momente) bleiben direkt in "Mein Leben", ohne eigene Unterkategorie.

**Noch zu erledigen:**
- [x] Alle Kategorien/Unterkategorien in WordPress angelegt (Beiträge → Kategorien)
- [x] BMI-Rechner-Beitrag von "Uncategorized" auf "Unverblümt" umgestellt
- [ ] Eigener Blocksy-Inhaltsblock (Content Block, Archiv-Hook) für die "Unverblümt"-Archivseite, ähnlich dem Hero-Aufbau beim BMI-Rechner

Inspiration/Ressourcen: [[04 Ressourcen/Social Media Wachstum/Social Media Wachstum.md|Social Media Wachstum]].

## Content-Ideen: persönlicher Blog (Rants über unehrliche Marketing-Praktiken)

Entscheidung 2026-09-25: siehe [[00 Kontext/Marketingmieze/ICP.md|ICP]] für den strategischen Hintergrund.

1. "Warum '10.000€ Umsatz in 30 Tagen'-Werbung dich anlügt (und wie das Spiel wirklich funktioniert)"
2. "Clickbait-Überschriften: Warum sie kurzfristig funktionieren und langfristig dein Image killen"
3. "Der Social-Proof-Trick, den fast jeder Coach nutzt – und warum er oft erfunden ist"
4. "Künstliche Verknappung ('nur noch 3 Plätze!') – wann sie ehrlich ist und wann Betrug"
5. "Warum die meisten 'organisches Wachstum'-Erfolgsgeschichten Bullshit sind"
6. "KI-generierter Content ohne Kennzeichnung: Wo die Grenze zur Verbrauchertäuschung verläuft"
7. "Fake-Bewertungen und gekaufte Follower: Wie man sie erkennt (aus erster Reihe)"
8. "Die Wahrheit über 'Persönliche Note' in Corporate-Marketing – wie viel davon ist wirklich persönlich?"

## Content-Ideen: persönlicher Blog, Serie "worüber keiner redet"

Entscheidung 2026-09-25: Zweiter Blog-Strang, unabhängig vom Job/Marketing-Winkel oben. Fokus: universelle, private Themen an der Schnittstelle Familie/Gesundheit/Geld, über die kaum offen gesprochen wird. Alle fünf sollen umgesetzt werden, Reihenfolge noch offen.

1. Die unsichtbare Care-Arbeit (Angehörige unterstützen/pflegen neben Job und eigenem Leben, "Sandwich-Generation")
2. Erschöpfung, die nichts mit Arbeit zu tun hat (leer sein wegen Familie/Organisation, obwohl "eigentlich alles im Griff")
3. Finanzielle Scham trotz eigentlich okay laufendem Leben (heimliche Vergleiche, Ungewissheit ob man's "richtig" macht)
4. Der Druck, für alle funktionieren zu müssen (Tochter, Partnerin, Kollegin, eigene Ziele gleichzeitig)
5. Einsamkeit, obwohl der Kalender voll ist (viele Menschen um einen herum, trotzdem allein mit den eigentlichen Sorgen)

Hinweis: Diese Themen können nah an privaten Bereichen (z.B. Pflege Mutter) liegen. Vor Veröffentlichung jeweils bewusst entscheiden, wie viel Privates konkret preisgegeben wird vs. verallgemeinert/anonymisiert.
