---
tags: [projekt, fairbeamtet]
status: entwurf
erstellt: 2026-11-13
---

# Familienzuschlag-Rechner (fairbeamtet.de)

## Ziel

Ein eigenständiger Familienzuschlag-Rechner für fairbeamtet.de, nach demselben Muster wie [[02 Projekte/Fairbeamtet/BMI-Rechner.md|BMI-Rechner]]: ein fokussiertes, eigenständig funktionierendes Tool statt des großen, noch nicht freigegebenen Beihilfe-/PKV-Lückenrechners aus [[02 Projekte/Fairbeamtet/Eigener Gehaltsrechner.md|Eigener Gehaltsrechner – Analyse & Konzept]].

Direkter Bezug zur Konkurrenzanalyse dort: Der Gehaltsrechner von einfachverbeamtet.de bringt laut [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]] rund ein Viertel des gesamten Konkurrenz-Traffics, und der Familienzuschlag ist einer der Eingabe-/Ausgabe-Bausteine dort. Eigene fairbeamtet.de-Seite zum Thema existiert bereits ([Familienzuschlag für Beamte: Höhe und Anspruch 2026](https://www.fairbeamtet.de/familienzuschlag-fuer-beamte/)), aber **ohne Rechner** – nur Text, Tabellen und zwei Beispielrechnungen. Dieses Tool löst das ein.

## Status

**Entwurf – noch nicht mit Sven abgestimmt. Zahlen sind Sekundärquellen-Recherche, noch nicht gegen die Landesbesoldungsgesetze (Primärquellen) geprüft.** Für mehrere Bundesländer sind die Werte zwischen Quellen widersprüchlich oder bei der Extraktion unklar geblieben (siehe „Bekannte Unsicherheiten" unten). **Vor Veröffentlichung zwingend:** Primärquellen-Check je Bundesland, analog zur Vorgabe beim BMI-Rechner (Rangfolge Voice Profile Punkt 1: fachliche Richtigkeit schlägt alles andere) – bei YMYL-Besoldungsdaten gilt das genauso wie bei Gesundheitsfragen.

## Rechtliche Grundlage

Bundesbeamte: § 40 BBesG. Landesbeamte: seit der Föderalismusreform 2006 die jeweiligen 16 Landesbesoldungsgesetze (eigene Anlagen zum Familienzuschlag, nicht mehr bundeseinheitlich). Das ist auch der Grund, warum die Struktur zwischen den Ländern so stark variiert (manche ganz ohne „Stufe 1", manche mit Besoldungsgruppen- oder Ortsklassen-/Mietenstufen-Abhängigkeit).

## Recherche: Familienzuschlag nach Bundesland (Stand der Recherche: 13.11.2026)

Recherchiert über mehrere Sekundärquellen (siehe Quellenliste unten), da eine vollständige Prüfung aller 16 Landesbesoldungsgesetze im Rahmen dieser Recherche nicht möglich war. **Die Quellen widersprechen sich bei mehreren Bundesländern** (unterschiedliche Stichtage, teils veraltete Werte, teils Extraktionsfehler bei komplexen Tabellen). Die folgende Tabelle ist die plausibelste Konsolidierung, aber **kein Ersatz für eine Gesetzesprüfung.**

| Bundesland | Stufe 1 (verheiratet/verpartnert) | Kinderanteil 1.+2. Kind (je Kind) | Ab 3. Kind (je Kind) | Gültig ab | Vertrauen |
|---|---|---|---|---|---|
| Bund | 181,36 € | 154,99 € | 482,89 € | 01.05.2026 | hoch (beide Quellen identisch) |
| Baden-Württemberg | 180,46 € | 157,78 € | 989,17 € | 01.04.2026 | mittel – zusätzlicher Familienergänzungszuschlag nach Besoldungsgruppe (A7–A10) nicht eingerechnet |
| Bayern | – | – | – | 01.10.2026 | **niedrig** – 7 Ortsklassen, Quellen widersprüchlich, kein sinnvoller Pauschalwert |
| Berlin | kein Stufe-1-Anteil (ggf. ~67,47 € Ausgleichszulage für Altfälle) | 148,44 € | 819,76 € (3. Kind) | 01.04.2026 | mittel |
| Brandenburg | kein Stufe-1-Anteil | 377,16 € | 888,39 € | 01.07.2024 | mittel – Datum wirkt älter als bei anderen Ländern |
| Bremen | ca. 157–165 € (besoldungsgruppenabhängig, A5–A8) | ca. 252–266 € | ca. 611 € | 01.04.2026 | niedrig |
| Hamburg | 165,84 € | 193,14 € | 635,00 € | 01.04.2026 | hoch – Werte intern konsistent (Stufen-Differenzen passen exakt) |
| Hessen | 177,30 € | 360,57 € | 831,08 € | 01.07.2026 | hoch – Werte intern konsistent, beide Quellen identisch |
| Mecklenburg-Vorpommern | 164,77 € | 198,83 € | 820,00 € | 01.04.2026 | hoch |
| Niedersachsen | 162,26 € (A5–A8; bis 170,36 € in höheren Gruppen) | 145,61 € | 512,37 € | 01.04.2026 | hoch |
| Nordrhein-Westfalen | – | – | – | 01.04.2026 | **niedrig** – zusätzlich Mietenstufen- (I–VII) und besoldungsgruppenabhängig, kein sinnvoller Pauschalwert |
| Rheinland-Pfalz | 88,03 € | 246,97 € | 726,00 € | 01.04.2026 | niedrig – Stufe-1-Wert wirkt im Ländervergleich ungewöhnlich niedrig |
| Saarland | 164,48 € | 165,31 € | 781,68 € | 01.04.2026 | hoch |
| Sachsen | 279,58 € | 279,58 € | 795,41 € | 01.04.2026 | hoch – beide Quellen identisch |
| Sachsen-Anhalt | 169,04 € | 184,85 € | 818,98 € | 01.04.2026 | mittel |
| Schleswig-Holstein | 176,24 € | 199,85 € | 516,48 € | 01.01.2026 | mittel – eine Quelle nennt stattdessen 164,21 € / 186,20 € zu einem älteren Stichtag (01.11.2024); neuerer Wert bevorzugt |
| Thüringen | 182,21 € | – | – | 01.04.2026 | **niedrig** – Kinderanteile in den Quellen widersprüchlich/unplausibel (u. a. identischer Wert für 3. und 4. Kind) |

### Quellen (Sekundärquellen, abgerufen 13.11.2026)

- [oeffentlichen-dienst.de – Familienzuschlag für Beamte 2026](https://www.oeffentlichen-dienst.de/beamte/besoldung/familienzuschlag.html)
- [beamtenberater.com – Familienzuschlag Beamte 2026](https://beamtenberater.com/familienzuschlag-beamte)
- [tarifvertrag-online.de – Familienzuschlag für Beamte 2026: Bund und alle 16 Länder](https://tarifvertrag-online.de/familienzuschlag)
- [fairbeamtet.de – Familienzuschlag für Beamte: Höhe und Anspruch 2026](https://www.fairbeamtet.de/familienzuschlag-fuer-beamte/) (eigener Artikel, nennt nur Bund + 2 Fallbeispiele, keine volle Länder-Tabelle)

## Bekannte Unsicherheiten / vor Launch zu klären

- **Bayern, Nordrhein-Westfalen**: strukturell zu komplex für einen einzelnen Pauschalwert (Ortsklassen bzw. Mietenstufen × Besoldungsgruppen). Entweder vor Launch die volle Matrix aus dem jeweiligen Landesbesoldungsgesetz einpflegen, oder in der ersten Version bewusst ausklammern und auf Beratung verweisen (siehe Rechner-Verhalten unten).
- **Thüringen**: Kinderanteile aus den Quellen nicht plausibel (Dritt- und Viertkind identischer Betrag) – eher Extraktionsfehler der Quelle als echter Gesetzeswert. Vor Launch direkt im Thüringer Besoldungsgesetz nachschlagen.
- **Rheinland-Pfalz**: Stufe-1-Betrag (88,03 €) liegt deutlich unter allen anderen Ländern (die sonst zwischen ~160–280 € liegen) – könnte ein Teilbetrag statt des vollen Satzes sein. Prüfen.
- **Bremen, Brandenburg**: nur eine grobe Spanne bzw. ältere Datenlage verfügbar.
- Mehrere Länder (Baden-Württemberg, Niedersachsen, Mecklenburg-Vorpommern, Bremen) haben zusätzliche „Familienergänzungszuschläge" nach Besoldungsgruppe, die hier **nicht** eingerechnet sind – das Tool rechnet nur den klassischen Familienzuschlag, nicht diese Zusatzkomponente. Sollte im Ergebnis als Fußnote stehen, damit niemand den Betrag für vollständig hält.
- **Bayern-Primärquelle gefunden, aber automatisiert nicht zuverlässig auslesbar**: Anlage 5 BayBesG ([gesetze-bayern.de](https://www.gesetze-bayern.de/Content/Document/BayBesG-ANL_5)) ist die amtliche Quelle, Landesamt für Finanzen Bayern veröffentlicht die aktuellen Beträge. Zwei automatisierte Abrufe derselben Tabelle (einmal direkt vom Gesetzestext, einmal über [tarifvertrag-online.de/familienzuschlag/bayern](https://tarifvertrag-online.de/familienzuschlag/bayern)) ergaben **deutlich unterschiedliche, teils in sich unplausible Zahlen** (z. B. nicht monoton steigend über die Ortsklassen, obwohl das inhaltlich so sein müsste). Das ist ein starkes Signal, dass die Bayern-Tabelle **manuell aus dem PDF/Gesetzestext abgelesen werden muss**, nicht per automatisiertem Seitenabruf – die Tabellenstruktur (mehrere Stufen × 7 Ortsklassen in einer Matrix) scheint dafür zu fehleranfällig.
- **NRW-Zwischenergebnis** (ein Datenpunkt, noch nicht gegen das Primärgesetz geprüft): Laut [besoldungsrechner.com](https://besoldungsrechner.com/nrw-familienzuschlag-mietenstufe-unterschiede) liegt der **Gesamt**-Familienzuschlag für Verheiratete ab A 9 bei 1 Kind zwischen 324,52 € (Mietenstufe I/II) und 955,05 € (Mietenstufe VII), bei 2 Kindern zwischen 734,08 € und 1.721,50 €. Diese Zahlen sind in sich konsistent (steigen monoton mit der Mietenstufe), aber eine einzelne Sekundärquelle – vor Verwendung gegen das NRW-Besoldungsgesetz prüfen.
- Generell: Jährliche/unterjährige Anpassungen (wie beim Bund zum 01.05., bei mehreren Ländern zum 01.04.) bedeuten **Pflegeaufwand**. Ohne jährlichen Update-Prozess veraltet der Rechner schnell – siehe dazu bereits die Risiken-Sektion in [[02 Projekte/Fairbeamtet/Eigener Gehaltsrechner.md|Eigener Gehaltsrechner]].

**Empfehlung:** Nicht live schalten, bevor mindestens die als „niedrig" markierten Länder (Bayern, NRW, Thüringen, Rheinland-Pfalz, Bremen) gegen das jeweilige Landesbesoldungsgesetz geprüft sind. Der Code unten ist entsprechend defensiv gebaut: Bundesländer ohne verlässliche Zahl liefern keine (falsche) Berechnung, sondern einen Hinweis + Beratungs-CTA.

## Uniqueness-Check: Was macht unseren Rechner besser als die Konkurrenz?

Recherchiert 13.11.2026, zweite Runde (gezielt nach existierenden *interaktiven* Rechnern für Bayern/NRW gesucht, nicht nur statischen Tabellen – Korrektur gegenüber der ersten Einschätzung unten).

- **beamtenberater.com, oeffentlichen-dienst.de (Hauptartikel), tarifvertrag-online.de**: nur statische Tabellen/Fließtext zum Familienzuschlag selbst, kein interaktiver Rechner dafür. Teils unvollständig (nur Stufe 1 + 1. Kind, weitere Kinder "auf Einzelseiten").
- **einfachverbeamtet.de**: hat laut [[02 Projekte/Fairbeamtet/Wettbewerbsanalyse.md|Wettbewerbsanalyse]] einen Familienzuschlag als Modul im großen Gehaltsrechner, aber nicht transparent in Methodik/Quellen.
- **Eigener fairbeamtet.de-Artikel**: nur Text + 2 Beispielrechnungen, kein eigenes Tool, genau wie beim BMI-Thema vor dem BMI-Rechner.

**Aber: Es gibt bereits mehrere Rechner, die Bayern und NRW trotz Ortsklassen-/Mietenstufen-Komplexität abdecken** – das ist kein unbesetztes Feld:
- **[Bezügerechner des BVA](https://bezuegerechner.bva.bund.de/rechner/beamte)**: offizieller Rechner des Bundesverwaltungsamts, aber nur für Bundesbeamte, nicht für Länder.
- **[oeffentlichen-dienst.de – Besoldungsrechner Bayern](https://www.oeffentlichen-dienst.de/beamte/besoldung/by/rechner.html)** und **[…NRW](https://www.oeffentlichen-dienst.de/beamte/besoldung/nrw/rechner.html)**: private Rechner mit Ortsklassen- bzw. Mietenstufen-Auswahl, berechnen die komplette Besoldung inkl. Familienzuschlag.
- **[besoldungsrechner.com/bayern](https://besoldungsrechner.com/bayern/)**: sehr detailliert – Besoldungsgruppe, Erfahrungsstufe, Ortsklasse (I–VII), Familienstand, "Partner im öffentlichen Dienst" (anteilige Regelung), Kinderzahl (0–8). Weist den Familienzuschlag in der Ergebnisübersicht **separat** aus ("Fam.Zuschlag Stufe V (Ehe)", "1. Kind", "2. Kind", "ab 3. Kind"). Kein Beratungs-CTA erkennbar, wirkt als reines Rechen-Tool ohne Lead-Mechanik.
- **[besoldungsrechner.com – NRW Mietenstufen-Überblick](https://besoldungsrechner.com/nrw-familienzuschlag-mietenstufe-unterschiede)**: eigene Tabellenseite nur zu diesem Thema, verweist auf den vollen Rechner.
- **[BBB-Rechner „Orts- und Familienzuschlag"](https://www.bbb-bayern.de/service/bbb-rechner-orts-und-familienzuschlag/)**: Rechner des Bayerischen Beamtenbunds, aber **nur für BBB-Mitglieder** zugänglich (App/Mitgliederportal), kein frei zugängliches Web-Tool. Nach eigener Aussage keine Günstigerprüfung und keine Nachzahlungsprüfung.
- **[tarifvertrag-online.de/familienzuschlag/nrw](https://tarifvertrag-online.de/familienzuschlag/nrw)** und **[…/bayern](https://tarifvertrag-online.de/familienzuschlag/bayern)**: statische Tabellen nach Mietenstufe/Ortsklasse, kein Rechner, aber immerhin vollständiger als die Hauptübersichtsseite.

**Einordnung:** Ein frei zugänglicher, werbefreier Rechner *speziell* für den Familienzuschlag (statt als Nebenprodukt eines kompletten Besoldungsrechners) existiert nicht. Die eigentliche Lücke ist also nicht "gibt es sowas schon", sondern: **kein Wettbewerber verbindet das mit Transparenz zu Datenqualität/Gültigkeit und einer ehrlichen Beratungs-CTA statt reiner Zahlenausgabe.** Unser Rechner sollte sich entsprechend positionieren – fokussiert auf den Familienzuschlag allein (schneller, einfacher als ein kompletter Besoldungsrechner mit 10+ Feldern), mit sichtbarem Gültigkeitsdatum/Vertrauens-Hinweis je Bundesland, und dort, wo die Datenlage nicht sauber ist (aktuell Bayern/NRW/Thüringen), ehrlich blockierend statt einen falschen Pseudo-Wert auszugeben.

## Rechner-Konzept

**Eingaben:**
- Bundesland (Dropdown, 17 Optionen: Bund + 16 Länder)
- Verheiratet/verpartnert (Ja/Nein)
- Anzahl kindergeldberechtigter Kinder (Zahl, 0–6+)

**Ausgabe:**
- Monatlicher Familienzuschlag, aufgeschlüsselt nach Ehe-/Partnerschaftsanteil und Kinderanteil
- Gültigkeitsdatum des verwendeten Werts
- Bei Bundesländern mit niedrigem Vertrauen oder fehlender Pauschalisierbarkeit: kein Zahlenwert, sondern Hinweistext + CTA zur Beratung
- Fußnote zu eventuellen Familienergänzungszuschlägen, die nicht eingerechnet sind

## Layout

Gleiche Markenbasis wie [[02 Projekte/Fairbeamtet/BMI-Rechner.md|BMI-Rechner]], damit beide Tools als zusammengehörige „Rechner-Familie" wirken: Anton für Headlines/große Zahlen, Inter für Fließtext, Navy `#0B1E33` als Hero-/Ergebnis-Hintergrund, Pink/Magenta `#FF3F77` als Akzent- und CTA-Farbe, Blau `#0693E3` für Formularelemente. Gleiches Karten-/Stat-Kachel-Muster, gleiche Kontaktkarte am Ende (Platzhalter-Kreise statt Fotos, wie beim BMI-Rechner).

## Code

Entwurf, fachlich **noch nicht freigegeben**. Die Datenbasis (`FZ_DATEN`) ist absichtlich so gebaut, dass Bundesländer mit `stufe1: null` oder `kind: null` keine Berechnung ausgeben, sondern einen Hinweis – das verhindert, dass unsichere Zahlen als Ergebnis ausgespielt werden, bevor der Primärquellen-Check gemacht ist.

```html
<div class="fb-fz-rechner">
  <div class="fb-fz-hero">
    <div class="fb-fz-hero-watermark" aria-hidden="true">€</div>
    <div class="fb-fz-hero-inner">
      <p class="fb-fz-eyebrow">FAMILIENZUSCHLAG 2026</p>
      <h1>DEIN ZUSCHLAG.<br><span class="fb-fz-accent">DEIN BUNDESLAND.</span></h1>
      <p class="fb-fz-intro">Verheiratet, verpartnert, mit Kindern? Der Familienzuschlag unterscheidet sich je Bundesland teils deutlich. Trag deine Situation ein, ich zeig dir deinen monatlichen Zuschlag.</p>
      <a href="#fbFzForm" class="fb-fz-hero-button">Jetzt berechnen <span aria-hidden="true">&rarr;</span></a>
    </div>
  </div>

  <div class="fb-fz-stat-row">
    <div class="fb-fz-stat-tile">
      <div class="fb-fz-stat-number">17</div>
      <p>Dienstherren (Bund + 16 Länder) mit jeweils eigener Besoldungsregel seit der Föderalismusreform 2006.</p>
    </div>
    <div class="fb-fz-stat-tile fb-fz-stat-tile-accent">
      <div class="fb-fz-stat-number">AB KIND 3</div>
      <p>In fast allen Bundesländern springt der Kinderanteil ab dem dritten Kind deutlich nach oben.</p>
    </div>
    <div class="fb-fz-stat-tile">
      <div class="fb-fz-stat-number">JÄHRLICH</div>
      <p>Die Beträge werden regelmäßig angepasst – meist zum 1. April, beim Bund zum 1. Mai.</p>
    </div>
  </div>

  <div class="fb-fz-grid">
    <div class="fb-fz-form-card" id="fbFzForm-anchor">
      <form id="fbFzForm">
        <div class="fb-fz-fields">
          <label class="fb-fz-field">
            Bundesland / Dienstherr
            <select id="fbFzLand" required>
              <option value="bund">Bund</option>
              <option value="bw">Baden-Württemberg</option>
              <option value="by">Bayern</option>
              <option value="be">Berlin</option>
              <option value="bb">Brandenburg</option>
              <option value="hb">Bremen</option>
              <option value="hh">Hamburg</option>
              <option value="he">Hessen</option>
              <option value="mv">Mecklenburg-Vorpommern</option>
              <option value="ni">Niedersachsen</option>
              <option value="nw">Nordrhein-Westfalen</option>
              <option value="rp">Rheinland-Pfalz</option>
              <option value="sl">Saarland</option>
              <option value="sn">Sachsen</option>
              <option value="st">Sachsen-Anhalt</option>
              <option value="sh">Schleswig-Holstein</option>
              <option value="th">Thüringen</option>
            </select>
          </label>

          <label class="fb-fz-field fb-fz-field-checkbox">
            <input type="checkbox" id="fbFzVerheiratet">
            Verheiratet / verpartnert
          </label>

          <label class="fb-fz-field">
            Anzahl kindergeldberechtigter Kinder
            <input type="number" id="fbFzKinder" min="0" max="10" step="1" value="0" required>
          </label>
        </div>

        <button type="submit" class="fb-fz-button">Berechnen</button>
      </form>
    </div>

    <div class="fb-fz-result-card">
      <div class="fb-fz-placeholder" id="fbFzPlaceholder">
        <p>Wähl links dein Bundesland und deine Familiensituation. Ich zeig dir deinen monatlichen Familienzuschlag.</p>
      </div>

      <div class="fb-fz-result" id="fbFzResult" hidden>
        <div class="fb-fz-number"><span id="fbFzValue">0</span><span class="fb-fz-unit">€/Monat</span></div>
        <div class="fb-fz-breakdown" id="fbFzBreakdown"></div>
        <p class="fb-fz-kommentar" id="fbFzKommentar"></p>
      </div>

      <div class="fb-fz-unklar" id="fbFzUnklar" hidden>
        <p id="fbFzUnklarText"></p>
        <a href="#" class="fb-fz-cta-button-inline">Meinen Zuschlag konkret klären lassen <span aria-hidden="true">&rarr;</span></a>
      </div>
    </div>
  </div>

  <div class="fb-fz-infobox">
    <h2>So funktioniert der Familienzuschlag</h2>
    <p>Der Familienzuschlag ergänzt deine Besoldung je nach Familienstand. Verheiratete oder verpartnerte Beamtinnen und Beamte erhalten die sogenannte Stufe 1. Für jedes kindergeldberechtigte Kind kommt zusätzlich ein kinderbezogener Anteil hinzu, der ab dem dritten Kind in fast allen Bundesländern deutlich höher ausfällt.</p>
    <p>Seit der Föderalismusreform 2006 legt jedes Bundesland seinen Familienzuschlag selbst im eigenen Landesbesoldungsgesetz fest – deshalb unterscheiden sich die Beträge teils erheblich, und manche Länder (z. B. Berlin, Brandenburg) zahlen gar keinen klassischen Ehe-/Partnerschaftsanteil mehr.</p>
    <p>Wichtig: Dieser Rechner bildet den <strong>klassischen</strong> Familienzuschlag ab. Mehrere Länder zahlen zusätzlich einen Familienergänzungszuschlag nach Besoldungsgruppe, der hier nicht eingerechnet ist. Bei Bayern und Nordrhein-Westfalen hängt der Betrag zusätzlich von Ortsklasse bzw. Mietenstufe ab – dafür geben wir hier bewusst keinen Pauschalwert aus. Mehr Hintergrund in unserem <a href="https://www.fairbeamtet.de/familienzuschlag-fuer-beamte/">ausführlichen Artikel zum Familienzuschlag</a>.</p>
  </div>

  <div class="fb-fz-contact-card">
    <div class="fb-fz-contact-photos" aria-hidden="true">
      <div class="fb-fz-contact-photo"></div>
      <div class="fb-fz-contact-photo"></div>
      <div class="fb-fz-contact-photo"></div>
    </div>
    <div class="fb-fz-contact-text">
      <p class="fb-fz-contact-label">DEINE ANSPRECHPARTNER</p>
      <h2>Fragen zu deiner Besoldung?</h2>
      <p>Der Familienzuschlag ist nur ein Baustein deiner Besoldung. Willst du wissen, was er für deine Vorsorge oder Absicherung bedeutet? Dann lass uns das gemeinsam klären, unverbindlich und kostenlos.</p>
      <a href="#" class="fb-fz-cta-button">Kostenloses Gespräch vereinbaren <span aria-hidden="true">&rarr;</span></a>
    </div>
  </div>
</div>

<style>
@import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');
/* Entwurfs-Hinweis: direkter Google-Fonts-Import ist nur fuer den Vorschlags-Entwurf okay.
   Vor Go-Live selbst hosten, siehe Layout-Entscheidungen im BMI-Rechner. */

.fb-fz-rechner {
  max-width: 1100px;
  margin: 0 auto;
  padding: 48px 24px;
  font-family: 'Inter', sans-serif;
  color: #1A1A1A;
}
.fb-fz-rechner h1,
.fb-fz-rechner h2,
.fb-fz-stat-number,
.fb-fz-number {
  font-family: 'Anton', 'Inter', sans-serif;
  font-weight: 400;
  text-transform: uppercase;
  letter-spacing: 0.01em;
}

.fb-fz-hero {
  position: relative;
  background: #0B1E33;
  color: #fff;
  border-radius: 20px;
  padding: 64px 40px;
  margin-bottom: 24px;
  text-align: center;
  overflow: hidden;
}
.fb-fz-hero-watermark {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-family: 'Anton', sans-serif;
  font-size: clamp(8rem, 28vw, 18rem);
  color: rgba(255,255,255,0.1) !important;
  white-space: nowrap;
  pointer-events: none;
  line-height: 1;
}
.fb-fz-hero-inner {
  position: relative;
  z-index: 1;
}
.fb-fz-eyebrow {
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  color: #7FC4F0 !important;
  margin: 0 0 16px 0;
}
.fb-fz-hero h1 {
  font-size: clamp(2.4rem, 6vw, 4.2rem);
  margin: 0 0 20px 0;
  line-height: 1.02;
  color: #fff !important;
}
.fb-fz-accent {
  color: #FF3F77 !important;
}
.fb-fz-hero .fb-fz-intro {
  max-width: 640px;
  margin: 0 auto;
  font-size: 1.1rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.9) !important;
}
.fb-fz-hero-button {
  display: inline-block;
  margin-top: 28px;
  background: #FF3F77;
  color: #fff;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 30px;
  font-family: 'Inter', sans-serif;
  font-weight: 700;
}
.fb-fz-hero-button:hover {
  background: #D92F5F;
}

.fb-fz-stat-row {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-bottom: 32px;
}
@media (max-width: 760px) {
  .fb-fz-stat-row {
    grid-template-columns: 1fr;
  }
}
.fb-fz-stat-tile {
  background: #F4F6FA;
  border-radius: 14px;
  padding: 24px;
}
.fb-fz-stat-tile-accent {
  background: #FF3F77;
  color: #fff;
}
.fb-fz-stat-tile-accent p {
  color: rgba(255,255,255,0.92);
}
.fb-fz-stat-number {
  font-size: 2rem;
  line-height: 1;
  margin-bottom: 8px;
}
.fb-fz-stat-tile p {
  margin: 0;
  font-size: 0.92rem;
  line-height: 1.5;
}

.fb-fz-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
  align-items: start;
  margin-bottom: 32px;
}

.fb-fz-form-card,
.fb-fz-result-card {
  border-radius: 16px;
  padding: 32px;
}
.fb-fz-form-card {
  background: #fff;
  border: 1px solid #E2E6EE;
  box-shadow: 0 10px 30px rgba(15,30,51,0.06);
}
.fb-fz-result-card {
  background: #0B1E33;
  color: #fff !important;
  min-height: 220px;
  padding: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.fb-fz-result-card * {
  color: inherit;
}

.fb-fz-fields {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-bottom: 20px;
}
@media (max-width: 560px) {
  .fb-fz-fields {
    grid-template-columns: 1fr;
  }
}
.fb-fz-field {
  display: flex;
  flex-direction: column;
  gap: 6px;
  font-weight: 600;
  font-size: 0.95rem;
}
.fb-fz-field-checkbox {
  flex-direction: row;
  align-items: center;
  gap: 10px;
}
.fb-fz-field select,
.fb-fz-field input[type="number"] {
  background: #fff !important;
  color: #1A1A1A !important;
  font-family: 'Inter', sans-serif;
  font-size: 1.05rem;
  padding: 14px 16px;
  border: 1px solid #D6DCE8;
  border-radius: 10px;
  box-sizing: border-box;
  width: 100%;
}
.fb-fz-field select:focus,
.fb-fz-field input:focus {
  outline: none;
  border-color: #0693E3;
}
.fb-fz-field input[type="checkbox"] {
  width: 20px;
  height: 20px;
  accent-color: #0693E3;
}

.fb-fz-button {
  font-family: 'Inter', sans-serif;
  background: #0693E3;
  color: #fff;
  border: none;
  border-radius: 999px;
  padding: 16px 28px;
  font-size: 1.05rem;
  font-weight: 700;
  cursor: pointer;
  width: 100%;
}
.fb-fz-button:hover {
  background: #057AB0;
}

.fb-fz-placeholder {
  text-align: center;
  font-size: 1.02rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.8) !important;
}
.fb-fz-placeholder p {
  color: inherit !important;
}
.fb-fz-result {
  text-align: center;
  width: 100%;
}
.fb-fz-number {
  font-size: 4.2rem;
  line-height: 1;
  color: #fff !important;
}
.fb-fz-unit {
  font-size: 1.4rem;
  margin-left: 8px;
  color: #FF6FB5 !important;
}
.fb-fz-breakdown {
  margin: 18px 0;
  font-family: 'Inter', sans-serif;
  text-transform: none;
  font-size: 0.95rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.85) !important;
}
.fb-fz-kommentar {
  font-size: 0.9rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.7) !important;
}
.fb-fz-unklar {
  text-align: center;
  width: 100%;
}
.fb-fz-unklar p {
  font-size: 1rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.9) !important;
  margin-bottom: 20px;
}
.fb-fz-cta-button-inline {
  display: inline-block;
  background: #FF3F77;
  color: #fff !important;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 28px;
  font-weight: 700;
  font-family: 'Inter', sans-serif;
}
.fb-fz-cta-button-inline:hover {
  background: #D92F5F;
}

.fb-fz-infobox {
  background: #F4F6FA;
  padding: 32px;
  border-radius: 16px;
  line-height: 1.6;
}
.fb-fz-infobox h2 {
  margin-top: 0;
  font-size: 1.7rem;
}

.fb-fz-contact-card {
  display: flex;
  gap: 24px;
  align-items: flex-start;
  background: #F4F6FA;
  border-radius: 16px;
  padding: 32px;
  margin-top: 24px;
}
@media (max-width: 560px) {
  .fb-fz-contact-card {
    flex-direction: column;
  }
}
.fb-fz-contact-photos {
  flex: 0 0 auto;
  display: flex;
}
.fb-fz-contact-photo {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  background: #0693E3;
  border: 3px solid #F4F6FA;
  margin-left: -16px;
}
.fb-fz-contact-photo:first-child {
  margin-left: 0;
  background: #9F4CFF;
}
.fb-fz-contact-photo:last-child {
  background: #FF3F77;
}
.fb-fz-contact-label {
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  color: #0693E3;
  margin: 0 0 4px 0;
}
.fb-fz-contact-text h2 {
  margin: 0 0 12px 0;
  font-size: 1.5rem;
  text-transform: none;
}
.fb-fz-contact-text p {
  margin: 0 0 16px 0;
  line-height: 1.6;
}
.fb-fz-cta-button {
  display: inline-block;
  background: #FF3F77;
  color: #fff;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 28px;
  font-weight: 700;
  font-family: 'Inter', sans-serif;
}
.fb-fz-cta-button:hover {
  background: #D92F5F;
}
</style>

<script>
(function() {
  // Stand der Recherche: 13.11.2026, Sekundärquellen – siehe Projektnotiz "Familienzuschlag-Rechner".
  // stufe1/kind/ab3 = null bedeutet: keine verlässliche Pauschalzahl verfügbar (Ortsklassen/Mietenstufen
  // oder widersprüchliche Quellen). In diesen Fällen wird bewusst NICHT gerechnet.
  var FZ_DATEN = {
    bund: { name: 'Bund', stufe1: 181.36, kind: 154.99, ab3: 482.89, gueltig: '01.05.2026', verlaesslich: true, hinweis: null },
    bw:   { name: 'Baden-Württemberg', stufe1: 180.46, kind: 157.78, ab3: 989.17, gueltig: '01.04.2026', verlaesslich: true, hinweis: 'Zusätzlicher Familienergänzungszuschlag nach Besoldungsgruppe (A 7–A 10) ist hier nicht eingerechnet.' },
    by:   { name: 'Bayern', stufe1: null, kind: null, ab3: null, gueltig: '01.10.2026', verlaesslich: false, hinweis: 'Bayern staffelt den Familienzuschlag nach 7 Ortsklassen – ein pauschaler Betrag wäre hier irreführend.' },
    be:   { name: 'Berlin', stufe1: 0, kind: 148.44, ab3: 819.76, gueltig: '01.04.2026', verlaesslich: true, hinweis: 'Berlin zahlt keinen klassischen Ehe-/Partnerschaftsanteil mehr (ggf. Ausgleichszulage für Altfälle, hier nicht eingerechnet).' },
    bb:   { name: 'Brandenburg', stufe1: 0, kind: 377.16, ab3: 888.39, gueltig: '01.07.2024', verlaesslich: false, hinweis: 'Brandenburg zahlt keinen ehebezogenen Anteil. Datenstand älter als bei den anderen Ländern – vor Verwendung prüfen.' },
    hb:   { name: 'Bremen', stufe1: 161.00, kind: 258.89, ab3: 610.60, gueltig: '01.04.2026', verlaesslich: false, hinweis: 'Richtwert – Bremen staffelt zusätzlich nach Besoldungsgruppe (A 5–A 8), der genaue Betrag kann abweichen.' },
    hh:   { name: 'Hamburg', stufe1: 165.84, kind: 193.14, ab3: 635.00, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    he:   { name: 'Hessen', stufe1: 177.30, kind: 360.57, ab3: 831.08, gueltig: '01.07.2026', verlaesslich: true, hinweis: null },
    mv:   { name: 'Mecklenburg-Vorpommern', stufe1: 164.77, kind: 198.83, ab3: 820.00, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    ni:   { name: 'Niedersachsen', stufe1: 162.26, kind: 145.61, ab3: 512.37, gueltig: '01.04.2026', verlaesslich: true, hinweis: 'Wert für Besoldungsgruppen A 5–A 8, in höheren Gruppen bis 170,36 € Stufe 1.' },
    nw:   { name: 'Nordrhein-Westfalen', stufe1: null, kind: null, ab3: null, gueltig: '01.04.2026', verlaesslich: false, hinweis: 'NRW staffelt zusätzlich nach Mietenstufe (I–VII) und Besoldungsgruppe – ein pauschaler Betrag wäre hier irreführend.' },
    rp:   { name: 'Rheinland-Pfalz', stufe1: 88.03, kind: 246.97, ab3: 726.00, gueltig: '01.04.2026', verlaesslich: false, hinweis: 'Der Stufe-1-Betrag wirkt im Ländervergleich ungewöhnlich niedrig – vor Veröffentlichung gegen das Landesbesoldungsgesetz prüfen.' },
    sl:   { name: 'Saarland', stufe1: 164.48, kind: 165.31, ab3: 781.68, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    sn:   { name: 'Sachsen', stufe1: 279.58, kind: 279.58, ab3: 795.41, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    st:   { name: 'Sachsen-Anhalt', stufe1: 169.04, kind: 184.85, ab3: 818.98, gueltig: '01.04.2026', verlaesslich: true, hinweis: null },
    sh:   { name: 'Schleswig-Holstein', stufe1: 176.24, kind: 199.85, ab3: 516.48, gueltig: '01.01.2026', verlaesslich: true, hinweis: null },
    th:   { name: 'Thüringen', stufe1: null, kind: null, ab3: null, gueltig: '01.04.2026', verlaesslich: false, hinweis: 'Die Kinderanteile sind in den verfügbaren Quellen widersprüchlich – vor Veröffentlichung gegen das Thüringer Besoldungsgesetz prüfen.' }
  };

  var form = document.getElementById('fbFzForm');
  var placeholder = document.getElementById('fbFzPlaceholder');
  var result = document.getElementById('fbFzResult');
  var unklar = document.getElementById('fbFzUnklar');
  var unklarText = document.getElementById('fbFzUnklarText');
  var valueEl = document.getElementById('fbFzValue');
  var breakdownEl = document.getElementById('fbFzBreakdown');
  var kommentarEl = document.getElementById('fbFzKommentar');

  function formatEuro(betrag) {
    return betrag.toLocaleString('de-DE', { minimumFractionDigits: 2, maximumFractionDigits: 2 });
  }

  form.addEventListener('submit', function(e) {
    e.preventDefault();

    var landKey = document.getElementById('fbFzLand').value;
    var verheiratet = document.getElementById('fbFzVerheiratet').checked;
    var kinder = parseInt(document.getElementById('fbFzKinder').value, 10) || 0;
    var daten = FZ_DATEN[landKey];

    if (daten.stufe1 === null || daten.kind === null) {
      placeholder.hidden = true;
      result.hidden = true;
      unklar.hidden = false;
      unklarText.textContent = 'Für ' + daten.name + ' lässt sich der Familienzuschlag nicht seriös pauschal berechnen: ' + daten.hinweis;
      return;
    }

    var eheAnteil = verheiratet ? daten.stufe1 : 0;
    var kinderAnteil = 0;
    for (var i = 1; i <= kinder; i++) {
      kinderAnteil += (i <= 2) ? daten.kind : daten.ab3;
    }
    var summe = eheAnteil + kinderAnteil;

    var zeilen = [];
    if (verheiratet) {
      zeilen.push('Ehe-/Partnerschaftsanteil (Stufe 1): ' + formatEuro(eheAnteil) + ' €');
    }
    if (kinder > 0) {
      zeilen.push('Kinderanteil für ' + kinder + ' Kind' + (kinder === 1 ? '' : 'er') + ': ' + formatEuro(kinderAnteil) + ' €');
    }
    if (zeilen.length === 0) {
      zeilen.push('Ohne Ehe-/Partnerschaft und ohne Kinder entsteht kein Familienzuschlag.');
    }

    valueEl.textContent = formatEuro(summe);
    breakdownEl.innerHTML = zeilen.map(function(z) { return '<div>' + z + '</div>'; }).join('');

    var kommentar = daten.name + ', gültig ab ' + daten.gueltig + '.';
    if (!daten.verlaesslich) {
      kommentar += ' Hinweis: ' + daten.hinweis;
    } else if (daten.hinweis) {
      kommentar += ' ' + daten.hinweis;
    }
    kommentarEl.textContent = kommentar;

    placeholder.hidden = true;
    unklar.hidden = true;
    result.hidden = false;
  });
})();
</script>
```

## Hinweise zur Einbindung

- Gleiche Schrift-/Farb-Basis wie [[02 Projekte/Fairbeamtet/BMI-Rechner.md|BMI-Rechner]] – siehe dort zu DSGVO-Pflicht beim Self-Hosting der Schrift vor Go-Live.
- Kontaktkarte mit Foto-Platzhaltern, analog zum BMI-Rechner – echte Fotos aus [[00 Kontext/Fairbeamtet/Team.md|Team]] einsetzen, sobald verfügbar.
- CTA-Links sind Platzhalter (`#`) – echte URL zur Beratungs-/Kontaktseite einsetzen.
- Die Datenstruktur `FZ_DATEN` ist bewusst so gebaut, dass sie sich künftig leicht aktualisieren lässt (ein Objekt pro Bundesland) – das deckt sich mit der in [[02 Projekte/Fairbeamtet/Eigener Gehaltsrechner.md|Eigener Gehaltsrechner]] geforderten zentralen Datenpflege statt händischer Einzelpflege pro Seite.

## Nächste Schritte

- [ ] Primärquellen-Check gegen die jeweiligen Landesbesoldungsgesetze – mindestens für die als „niedrig" markierten Länder (Bayern, NRW, Thüringen, Rheinland-Pfalz, Bremen, Brandenburg)
- [ ] Entscheiden, wie mit Bayern/NRW umgegangen wird: volle Ortsklassen-/Mietenstufen-Matrix einpflegen oder bewusst nur mit Hinweistext + CTA arbeiten (aktueller Stand im Code)
- [ ] Mit Sven abstimmen: fachliche Freigabe der Zahlen, Platzierung auf der Seite (eigenständige Rechner-Seite vs. Einbindung im bestehenden Artikel)
- [ ] Echten Link zur Beratungs-/Kontaktseite einsetzen
- [ ] Jährlichen Update-Prozess für die Zahlen festlegen (mehrere Länder passen zum 1. April an, der Bund zum 1. Mai)
- [ ] Erst nach Freigabe: live schalten
