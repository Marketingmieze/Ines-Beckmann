---
tags: [projekt, fairbeamtet]
status: entwurf
erstellt: 2026-11-12
---

# BMI-Rechner (fairbeamtet.de)

## Ziel

Ein BMI-Rechner für fairbeamtet.de im Kontext PKV-Gesundheitsprüfung, als eigenständiges Tool – unabhängig vom größeren geplanten Beihilfe-/PKV-Lückenrechner aus [[02 Projekte/Fairbeamtet/Eigener Gehaltsrechner.md|Eigener Gehaltsrechner – Analyse & Konzept]]. Status dort weiterhin offen (Sven-Freigabe aussteht) – dieser Rechner hier ist ein **eigenständiger Entwurf zum Vorschlagen**, kein freigegebenes Projekt.

Herkunft der Idee: ursprünglich für marketingmieze.com gebaut (siehe [[02 Projekte/Marketingmieze/BMI-Rechner.md|BMI-Rechner Marketingmieze]]), jetzt als eigenständige, fachlich und stilistisch komplett neue Version für fairbeamtet.de. **Keine Inhalte von dort übernommen** – andere Zielgruppe, anderer Ton, andere rechtliche Anforderungen (YMYL, PKV-Gesundheitsprüfung).

## Status

Entwurf – noch nicht mit Sven abgestimmt. Fachliche Zahlen (BMI-Schwellenwerte, Risikozuschläge) stammen aus Sekundärquellen (Vergleichsportale), nicht aus Primärquellen. **Vor Veröffentlichung: Faktencheck mit Sven/fachliche Prüfung zwingend**, siehe Rangfolge in [[04 Ressourcen/Schreibregeln/fairbeamtet Voice Profile.md|Voice Profile]] Punkt 1 (fachliche Richtigkeit schlägt alles andere).

## Autor/Stimme

Sven Höhne, Ich-Form, 26 Jahre Erfahrung (laut Voice Profile Abschnitt 2 die Zahl, die er selbst nutzt).

## Rechercheergebnis (2026-11-12, Sekundärquellen, nicht primärquellengeprüft)

- Unter BMI 30: in der Regel kein Zuschlag wegen Gewichts allein.
- Ab BMI 30 (Adipositas Grad I): praktisch alle Versicherer verlangen einen Risikozuschlag, grob 10–40/50 % auf den Grundbeitrag, je nach Versicherer.
- Ab BMI 35 (Adipositas Grad II): laut einer Quelle lehnen über 85 % der Versicherer kategorisch ab.
- Ab BMI 40: meist Ablehnung.
- Schwellenwerte unterscheiden sich je Versicherer teils deutlich (Beispiel aus der Recherche: Signal Iduna bereits ab BMI 25, Alte Oldenburger/Barmenia erst ab 30).

Quellen (Sekundärquellen, Stand der Recherche 12.11.2026, vor Veröffentlichung mit Primärquellen/Sven abgleichen):
- [KVoptimal.de – Trotz Übergewicht eine PKV finden](https://kvoptimal.de/blog/private-krankenversicherung/trotz-uebergewicht-eine-pkv-finden/)
- [covago.de – PKV mit Übergewicht](https://covago.de/pkv-mit-uebergewicht/)
- [covago.de – Risikozuschlag PKV Übergewicht](https://covago.de/risikozuschlag-pkv-uebergewicht/)
- [pkvmitplan.de – PKV mit Übergewicht](https://pkvmitplan.de/vorerkrankungen/pkv-mit-uebergewicht/)
- [elbland-finanz.de – PKV trotz Übergewicht](https://elbland-finanz.de/pkv-trotz-uebergewicht/)
- [pkvmitsystem.com – PKV trotz Übergewicht](https://pkvmitsystem.com/pkv-uebergewicht/)

## Einordnung zum eigenen Angebot

Der natürliche CTA ist nicht nur "Beratungstermin", sondern konkret die **anonyme Risikovoranfrage** aus [[00 Kontext/Fairbeamtet/Angebot.md|Angebot]] – die klärt die tatsächlichen Konditionen bei einem konkreten Versicherer, ohne dass der Interessent sich festlegt. Das ist der ehrliche nächste Schritt, weil der Rechner selbst nur grobe Richtwerte liefern kann (siehe Rangfolge Fachlichkeit vor Verkauf).

## Layout-Entscheidungen (2026-11-12)

- Farben: echte Marken-Hex-Werte, 2026-11-12 direkt aus dem HTML von fairbeamtet.de extrahiert (nicht geschätzt): `#0693E3` Blau, `#FF3F77` Pink/Magenta, `#1A1A1A` Dunkelgrund. Ergänzende Töne (helleres Blau, Lila-Akzent für den Gauge-Übergang) von diesen drei Grundfarben abgeleitet, da im Branding-Dokument keine weiteren definiert sind.
- Kein Gender-Toggle (anders als bei der Marketingmieze-Version) – die BMI-Formel selbst ist geschlechtsneutral, und die recherchierten PKV-Schwellenwerte unterscheiden nicht nach Geschlecht.
- Gauge-Segmente bewusst an der PKV-Logik ausgerichtet, nicht nur an den WHO-Kategorien: "Übergewicht" endet bei BMI 30, genau an der Schwelle, ab der laut Recherche so gut wie alle Versicherer einen Zuschlag ansetzen. Die Farbe kippt an dieser Stelle von Blau auf Pink/Magenta (Signalfarbe für "jetzt handeln/anonym anfragen").
- CTA-Button führt zur anonymen Risikovoranfrage (Platzhalter-Link `#`, echte URL noch einsetzen), nicht zu einem generischen Kontaktformular.

### Redesign 2026-11-12: Stil-Referenz "die Bayerische – Altersvorsorgedepot Landingpage"

Ines hat eine Referenz-Landingpage (PDF in 01 Inbox) mitgebracht: große, fette, eng gesetzte Großbuchstaben-Headlines, dunkle Navy-Flächen im Wechsel mit hellen Abschnitten, Stat-Kacheln mit riesigen Zahlen, ein großes verblasstes Hintergrund-Element hinter der Hero-Headline, Pill-Buttons mit Pfeil, eine persönliche Ansprechpartner-Karte am Ende. Layout jetzt entsprechend umgebaut, mit den echten fairbeamtet-Farben statt dem Orange des Vorbilds:

- **Anton** (Google Font, sehr fett, eng, passend zur Referenz) für alle Headlines/große Zahlen, **Inter** weiterhin für Fließtext.
- Hero: dunkles Navy (`#0B1E33`, aus Schwarz + Markenblau gemischt, näher am Vorbild als reines `#1A1A1A`), großes verblasstes "BMI"-Wasserzeichen im Hintergrund, Pfeil-Button runter zum Formular.
- Neue Stat-Kachel-Reihe direkt unter dem Hero (analog zu den "14,7 Mio. / 120 € / 540 €"-Kacheln im Vorbild): drei Kernzahlen aus der Recherche, mittlere/rechte Kachel in Pink/Magenta hervorgehoben.
- Ergebnis-Karte umgebaut zur großen Stat-Kachel mit riesiger Anton-Zahl statt nur mittelgroßer Zahl.
- Abschluss-Bereich als Ansprechpartner-Karte, analog zur "Dominik Brandt"-Karte im Vorbild, statt nur Fließtext + Button.

**Wichtig, aus der Marketingmieze-Erfahrung übernommen:** Der Code lädt "Anton" aktuell per `@import` direkt von `fonts.googleapis.com` – das ist für den Entwurf zum Vorschlagen okay, aber **vor einem echten Go-Live DSGVO-technisch nicht sauber** (siehe die ganze Schriften-Odyssee bei marketingmieze.com). Vor Veröffentlichung muss die Schrift genauso selbst gehostet werden wie dort am Ende gelöst.

### Korrekturen nach erstem Praxistest (2026-11-12)

Ines hat den ersten Entwurf live angeschaut, vier Korrekturen:

1. **Hero-Text war unlesbar.** Die H1 und der Intro-Absatz haben die weiße Schriftfarbe nicht geerbt (vermutlich Theme-CSS mit höherer Spezifität, derselbe Bug-Typ wie bei der ganzen Schriften-Odyssee auf marketingmieze.com). Jetzt mit `!important` fest auf Weiß gesetzt.
2. **Mythos-Zitat-Box komplett entfernt.** Ines wollte "nichts als Zitat" – die Kernaussage steckt eh schon in der ersten Stat-Kachel ("<30 kein Zuschlag"), keine Doppelung nötig.
3. **Formular- und Ergebnis-Karte stehen jetzt untereinander statt nebeneinander**, beide auf voller Breite. Die Ergebnis-Karte hat dadurch deutlich mehr Platz (größere Zahl, breitere Gauge).
4. **Kontaktkarte zeigt jetzt das ganze PKV-/DU-Team statt nur Sven.** Drei überlappende Platzhalter-Kreise statt einem Einzelfoto, Text auf "wir" umgestellt. Bei Bedarf später durch echte Fotos aus [[00 Kontext/Fairbeamtet/Team.md|Team]] ersetzen (Michael Buchholz, Sven Höhne, Christian Beine, Elenor Habtezghi, Luisa Bensmaya, Nicole Scheller, Sebastian Gottschalk für PKV; Dennis Kaspers, Sven Dottermann für BU/DU).

### Gauge-Nachbesserung (2026-11-12, zweite Runde)

Die Segmente "Normal" und "Über" waren bei exakter BMI-Skalierung (15–45) kaum sichtbar, weil "Adipositas" allein die Hälfte der Breite einnahm. Jetzt visuell ausgewogene, feste Segmentbreiten (15 % Unter, 30 % Normal, 20 % Über, 35 % Adipositas) statt reiner Zahlen-Proportionalität. Damit der Marker trotzdem exakt in der richtig angezeigten Farbzone landet, rechnet `markerPosition()` jetzt abschnittsweise (eigene lineare Interpolation je Zone) statt mit einer einzigen linearen Formel über die ganze Skala.

## Nächste Schritte

- [x] Code-Entwurf (Layout) erstellt
- [x] Echte Marken-Hex-Werte von fairbeamtet.de eingesetzt (aus der Live-Seite extrahiert, 12.11.2026)
- [ ] Echten Link zur Risikovoranfrage-Seite einsetzen
- [ ] Sven zur fachlichen Prüfung vorlegen (Zahlen, Schwellenwerte, Rechtssicherheit, Texte)
- [ ] Erst nach Freigabe: Mascot-Visual erstellen (Branding: Funko-Pop-Style "Sven"-Maskottchen)
- [ ] Erst nach Freigabe: live schalten

## Code

Entwurf, noch nicht fachlich geprüft. Layout fokussiert, Texte können sich noch ändern.

```html
<div class="fb-bmi-rechner">
  <div class="fb-bmi-hero">
    <div class="fb-bmi-hero-watermark" aria-hidden="true">BMI</div>
    <div class="fb-bmi-hero-inner">
      <p class="fb-bmi-eyebrow">BMI &amp; PKV-GESUNDHEITSPRÜFUNG</p>
      <h1>DEIN BMI.<br><span class="fb-bmi-accent">DEINE ZAHL.</span></h1>
      <p class="fb-bmi-intro">Du willst wissen, ob dein Gewicht beim PKV-Abschluss zum Problem wird? Dein BMI ist der erste Wert, den jeder Versicherer bei der Gesundheitsprüfung ansieht. Rechne ihn hier aus. Dann zeig ich dir, was die Zahl für dich bedeutet.</p>
      <a href="#fbBmiForm" class="fb-bmi-hero-button">Jetzt berechnen <span aria-hidden="true">&rarr;</span></a>
    </div>
  </div>

  <div class="fb-bmi-stat-row">
    <div class="fb-bmi-stat-tile">
      <div class="fb-bmi-stat-number">&lt;30</div>
      <p>Bis hierhin verlangt praktisch kein Versicherer einen Zuschlag wegen des Gewichts allein.</p>
    </div>
    <div class="fb-bmi-stat-tile fb-bmi-stat-tile-accent">
      <div class="fb-bmi-stat-number">10&ndash;40%</div>
      <p>Grober Risikozuschlag, den die meisten Versicherer ab BMI 30 auf den Beitrag aufschlagen.</p>
    </div>
    <div class="fb-bmi-stat-tile">
      <div class="fb-bmi-stat-number">&ge;40</div>
      <p>Ab diesem Wert wird eine Aufnahme bei den meisten Versicherern eng.</p>
    </div>
  </div>

  <div class="fb-bmi-grid">
    <div class="fb-bmi-form-card" id="fbBmiForm-anchor">
      <form id="fbBmiForm">
        <div class="fb-bmi-fields">
          <label class="fb-bmi-field">
            Alter in Jahren
            <input type="number" id="fbAlter" min="1" max="120" required>
          </label>

          <label class="fb-bmi-field">
            Größe in cm
            <input type="number" id="fbGroesse" min="50" max="250" required>
          </label>

          <label class="fb-bmi-field">
            Gewicht in kg
            <input type="number" id="fbGewicht" min="20" max="400" step="0.1" required>
          </label>
        </div>

        <button type="submit" class="fb-bmi-button">Berechnen</button>
      </form>
    </div>

    <div class="fb-bmi-result-card">
      <div class="fb-bmi-placeholder" id="fbBmiPlaceholder">
        <p>Trag links deine Werte ein. Ich zeig dir, was deine Zahl für die PKV bedeutet.</p>
      </div>

      <div class="fb-bmi-result" id="fbBmiResult" hidden>
        <div class="fb-bmi-number"><span id="fbBmiValue">0</span></div>
        <div class="fb-bmi-kategorie" id="fbBmiKategorie"></div>

        <div class="fb-bmi-gauge">
          <div class="fb-bmi-gauge-track">
            <span class="fb-bmi-segment fb-bmi-segment-unter"></span>
            <span class="fb-bmi-segment fb-bmi-segment-normal"></span>
            <span class="fb-bmi-segment fb-bmi-segment-ueber"></span>
            <span class="fb-bmi-segment fb-bmi-segment-adipositas"></span>
            <div class="fb-bmi-marker" id="fbBmiMarker"></div>
          </div>
          <div class="fb-bmi-gauge-labels">
            <span class="fb-bmi-label-unter">Unter</span><span class="fb-bmi-label-normal">Normal</span><span class="fb-bmi-label-ueber">Über</span><span class="fb-bmi-label-adipositas">Ab hier Zuschlag</span>
          </div>
        </div>

        <p class="fb-bmi-kommentar" id="fbBmiKommentar"></p>
      </div>
    </div>
  </div>

  <div class="fb-bmi-infobox">
    <h2>So rechnet sich dein BMI, und das bedeutet er für deine PKV</h2>
    <p>Der BMI teilt dein Gewicht in Kilogramm durch deine Größe in Metern zum Quadrat. Mehr steckt rechnerisch nicht dahinter. Für Versicherer ist er trotzdem der erste Blick, bevor sie genauer hinschauen: Vorerkrankungen, Blutwerte, dein Lebensstil.</p>

    <p>Unter BMI 30 prüfen Versicherer dein Gewicht meist ohne Zuschlag. Ab 30 kalkulieren fast alle einen Risikozuschlag ein, je nach Versicherer zwischen 10 und 50 Prozent auf deinen Beitrag. Ab 35 lehnen einige Versicherer ab. Ab 40 wird es für die meisten eng.</p>

    <p>Wichtig: Jeder Versicherer zieht die Grenze anders. Die Signal Iduna schaut schon ab 25 genauer hin. Die Alte Oldenburger und die Barmenia erst ab 30. Die Zahlen hier sind Richtwerte, keine Zusage für deinen Fall.</p>

  </div>

  <div class="fb-bmi-contact-card">
    <div class="fb-bmi-contact-photos" aria-hidden="true">
      <div class="fb-bmi-contact-photo"></div>
      <div class="fb-bmi-contact-photo"></div>
      <div class="fb-bmi-contact-photo"></div>
    </div>
    <div class="fb-bmi-contact-text">
      <p class="fb-bmi-contact-label">DEINE ANSPRECHPARTNER</p>
      <h2>Unser PKV- und DU-Team</h2>
      <p>Willst du wissen, was dein BMI bei einem konkreten Versicherer tatsächlich bedeutet? Dann fragen wir das für dich anonym an. Du bekommst eine echte Antwort, ohne dass irgendwo dein Name auftaucht und ohne dass du dich festlegst.</p>
      <a href="#" class="fb-bmi-cta-button">Meine Chancen anonym klären lassen <span aria-hidden="true">&rarr;</span></a>
    </div>
  </div>
</div>

<style>
@import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');
/* Entwurfs-Hinweis: direkter Google-Fonts-Import ist nur fuer den Vorschlags-Entwurf okay.
   Vor Go-Live selbst hosten, siehe Layout-Entscheidungen oben (DSGVO). */

.fb-bmi-rechner {
  max-width: 1100px;
  margin: 0 auto;
  padding: 48px 24px;
  font-family: 'Inter', sans-serif;
  color: #1A1A1A;
}
.fb-bmi-rechner h1,
.fb-bmi-rechner h2,
.fb-bmi-stat-number,
.fb-bmi-number {
  font-family: 'Anton', 'Inter', sans-serif;
  font-weight: 400;
  text-transform: uppercase;
  letter-spacing: 0.01em;
}

.fb-bmi-hero {
  position: relative;
  background: #0B1E33;
  color: #fff;
  border-radius: 20px;
  padding: 64px 40px;
  margin-bottom: 24px;
  text-align: center;
  overflow: hidden;
}
.fb-bmi-hero-watermark {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-family: 'Anton', sans-serif;
  font-size: clamp(8rem, 28vw, 18rem);
  color: rgba(255,255,255,0.04);
  white-space: nowrap;
  pointer-events: none;
  line-height: 1;
}
.fb-bmi-hero-inner {
  position: relative;
  z-index: 1;
}
.fb-bmi-eyebrow {
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  color: #7FC4F0 !important;
  margin: 0 0 16px 0;
}
.fb-bmi-hero h1 {
  font-size: clamp(2.4rem, 6vw, 4.2rem);
  margin: 0 0 20px 0;
  line-height: 1.02;
  color: #fff !important;
}
.fb-bmi-accent {
  color: #FF3F77 !important;
}
.fb-bmi-hero .fb-bmi-intro {
  max-width: 640px;
  margin: 0 auto;
  font-size: 1.1rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.9) !important;
}
.fb-bmi-hero-button {
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
.fb-bmi-hero-button:hover {
  background: #D92F5F;
}

.fb-bmi-stat-row {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-bottom: 32px;
}
@media (max-width: 760px) {
  .fb-bmi-stat-row {
    grid-template-columns: 1fr;
  }
}
.fb-bmi-stat-tile {
  background: #F4F6FA;
  border-radius: 14px;
  padding: 24px;
}
.fb-bmi-stat-tile-accent {
  background: #FF3F77;
  color: #fff;
}
.fb-bmi-stat-tile-accent p {
  color: rgba(255,255,255,0.92);
}
.fb-bmi-stat-number {
  font-size: 2.6rem;
  line-height: 1;
  margin-bottom: 8px;
}
.fb-bmi-stat-tile p {
  margin: 0;
  font-size: 0.92rem;
  line-height: 1.5;
}

.fb-bmi-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
  align-items: start;
  margin-bottom: 32px;
}

.fb-bmi-form-card,
.fb-bmi-result-card {
  border-radius: 16px;
  padding: 32px;
}
.fb-bmi-form-card {
  background: #fff;
  border: 1px solid #E2E6EE;
  box-shadow: 0 10px 30px rgba(15,30,51,0.06);
}
.fb-bmi-result-card {
  background: #0B1E33;
  color: #fff;
  min-height: 220px;
  padding: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.fb-bmi-fields {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-bottom: 20px;
}
@media (max-width: 560px) {
  .fb-bmi-fields {
    grid-template-columns: 1fr;
  }
}
.fb-bmi-field {
  display: flex;
  flex-direction: column;
  gap: 6px;
  font-weight: 600;
  font-size: 0.95rem;
}
.fb-bmi-field input {
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
.fb-bmi-field input:focus {
  outline: none;
  border-color: #0693E3;
}

.fb-bmi-button {
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
.fb-bmi-button:hover {
  background: #057AB0;
}

.fb-bmi-placeholder {
  text-align: center;
  font-size: 1.02rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.8);
}
.fb-bmi-result {
  text-align: center;
  width: 100%;
}
.fb-bmi-number {
  font-size: 6rem;
  line-height: 1;
}
.fb-bmi-kategorie {
  font-size: 1.1rem;
  font-weight: 700;
  margin-top: 8px;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  color: #FF6FB5;
}
.fb-bmi-gauge {
  margin: 22px 0;
}
.fb-bmi-gauge-track {
  position: relative;
  display: flex;
  height: 12px;
  border-radius: 999px;
  overflow: visible;
}
.fb-bmi-segment {
  display: block;
  height: 100%;
}
.fb-bmi-segment-unter {
  flex: 0 0 15%;
  background: #7FC4F0;
  border-radius: 999px 0 0 999px;
}
.fb-bmi-segment-normal {
  flex: 0 0 30%;
  background: #0693E3;
}
.fb-bmi-segment-ueber {
  flex: 0 0 20%;
  background: #9F4CFF;
}
.fb-bmi-segment-adipositas {
  flex: 0 0 35%;
  background: #FF3F77;
  border-radius: 0 999px 999px 0;
}
.fb-bmi-marker {
  position: absolute;
  top: -6px;
  left: 0%;
  width: 4px;
  height: 24px;
  background: #fff;
  border-radius: 2px;
  box-shadow: 0 0 0 2px #1A1A1A;
  transition: left 0.4s ease;
}
.fb-bmi-gauge-labels {
  display: flex;
  font-size: 0.72rem;
  font-weight: 700;
  margin-top: 8px;
}
.fb-bmi-gauge-labels span {
  text-align: center;
}
.fb-bmi-label-unter {
  flex: 0 0 15%;
  color: #7FC4F0;
}
.fb-bmi-label-normal {
  flex: 0 0 30%;
  color: #4DB8F5;
}
.fb-bmi-label-ueber {
  flex: 0 0 20%;
  color: #C98FFF;
}
.fb-bmi-label-adipositas {
  flex: 0 0 35%;
  color: #FF6FB5;
}
.fb-bmi-kommentar {
  font-size: 1rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.92);
}

.fb-bmi-infobox {
  background: #F4F6FA;
  padding: 32px;
  border-radius: 16px;
  line-height: 1.6;
}
.fb-bmi-infobox h2 {
  margin-top: 0;
  font-size: 1.7rem;
}

.fb-bmi-contact-card {
  display: flex;
  gap: 24px;
  align-items: flex-start;
  background: #F4F6FA;
  border-radius: 16px;
  padding: 32px;
  margin-top: 24px;
}
@media (max-width: 560px) {
  .fb-bmi-contact-card {
    flex-direction: column;
  }
}
.fb-bmi-contact-photos {
  flex: 0 0 auto;
  display: flex;
}
.fb-bmi-contact-photo {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  background: #0693E3;
  border: 3px solid #F4F6FA;
  margin-left: -16px;
}
.fb-bmi-contact-photo:first-child {
  margin-left: 0;
  background: #9F4CFF;
}
.fb-bmi-contact-photo:last-child {
  background: #FF3F77;
}
.fb-bmi-contact-label {
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  color: #0693E3;
  margin: 0 0 4px 0;
}
.fb-bmi-contact-text h2 {
  margin: 0 0 12px 0;
  font-size: 1.5rem;
  text-transform: none;
}
.fb-bmi-contact-text p {
  margin: 0 0 16px 0;
  line-height: 1.6;
}
.fb-bmi-cta-button {
  display: inline-block;
  background: #FF3F77;
  color: #fff;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 28px;
  font-weight: 700;
  font-family: 'Inter', sans-serif;
}
.fb-bmi-cta-button:hover {
  background: #D92F5F;
}
</style>

<script>
(function() {
  var form = document.getElementById('fbBmiForm');
  var placeholder = document.getElementById('fbBmiPlaceholder');
  var result = document.getElementById('fbBmiResult');
  var valueEl = document.getElementById('fbBmiValue');
  var kategorieEl = document.getElementById('fbBmiKategorie');
  var kommentarEl = document.getElementById('fbBmiKommentar');
  var markerEl = document.getElementById('fbBmiMarker');

  // Abschnittsweise Positionsberechnung, passend zu den visuellen Segmentbreiten
  // (15% Unter, 30% Normal, 20% Über, 35% Adipositas) statt reiner linearer BMI-Skala.
  // So bleibt der Marker immer exakt in der Farbzone, die auch angezeigt wird.
  function markerPosition(bmi) {
    if (bmi <= 15) return 0;
    if (bmi < 18.5) return (bmi - 15) / (18.5 - 15) * 15;
    if (bmi < 25) return 15 + (bmi - 18.5) / (25 - 18.5) * 30;
    if (bmi < 30) return 45 + (bmi - 25) / (30 - 25) * 20;
    if (bmi <= 45) return 65 + (bmi - 30) / (45 - 30) * 35;
    return 100;
  }

  function kategorisieren(bmi) {
    if (bmi < 18.5) {
      return { label: 'Untergewicht', text: 'Dein BMI liegt unter dem Normalbereich. Das löst bei den meisten Versicherern keinen Zuschlag aus, kann aber Rückfragen zur Ursache nach sich ziehen.' };
    } else if (bmi < 25) {
      return { label: 'Normalgewicht', text: 'Dein BMI liegt im unauffälligen Bereich. Versicherer verlangen hier in der Regel keinen BMI-bedingten Zuschlag.' };
    } else if (bmi < 30) {
      return { label: 'Übergewicht', text: 'Noch kein automatischer Zuschlag bei den meisten Versicherern. Einzelne, zum Beispiel die Signal Iduna, schauen schon ab 25 genauer hin.' };
    } else if (bmi < 35) {
      return { label: 'Ab hier Zuschlag wahrscheinlich', text: 'Ab BMI 30 kalkulieren fast alle Versicherer einen Risikozuschlag ein, grob 10 bis 40 Prozent auf deinen Beitrag, je nach Versicherer.' };
    } else if (bmi < 40) {
      return { label: 'Zuschlag oder Ablehnung möglich', text: 'In diesem Bereich lehnen einzelne Versicherer bereits ab. Andere verlangen einen höheren Zuschlag. Eine anonyme Risikovoranfrage zeigt dir, wo du stehst.' };
    } else {
      return { label: 'Für die meisten Versicherer eng', text: 'Ab BMI 40 wird es für die meisten Versicherer eng. Eine anonyme Risikovoranfrage zeigt dir trotzdem, welche Versicherer dich zu welchen Konditionen nehmen.' };
    }
  }

  form.addEventListener('submit', function(e) {
    e.preventDefault();
    var groesseCm = parseFloat(document.getElementById('fbGroesse').value);
    var gewichtKg = parseFloat(document.getElementById('fbGewicht').value);

    if (!groesseCm || !gewichtKg || groesseCm <= 0 || gewichtKg <= 0) {
      return;
    }

    var groesseM = groesseCm / 100;
    var bmi = gewichtKg / (groesseM * groesseM);
    var kategorie = kategorisieren(bmi);

    valueEl.textContent = bmi.toFixed(1);
    kategorieEl.textContent = kategorie.label;
    kommentarEl.textContent = kategorie.text;
    markerEl.style.left = markerPosition(bmi) + '%';

    placeholder.hidden = true;
    result.hidden = false;
  });
})();
</script>
```

## Hinweise zur Einbindung

- Schriften: "Inter" für Fließtext (angenommen, siehe Branding-Notiz "klare, moderne serifenlose Schrift"), "Anton" für Headlines/große Zahlen (neu seit dem Redesign im Stil der "die Bayerische"-Referenz). Beide aktuell per `@import` von Google geladen – **nur für den Entwurf okay, vor Go-Live selbst hosten** (DSGVO, siehe Layout-Entscheidungen).
- Farben sind echte fairbeamtet-Marken-Hex-Werte (siehe Layout-Entscheidungen oben), keine Platzhalter mehr.
- Kontaktkarte am Ende hat einen **Foto-Platzhalter** (blauer Kreis statt echtem Bild) – echtes Sven-Foto/Maskottchen einsetzen, sobald verfügbar.
- Kein Mascot/Bild im Hero integriert – kommt erst nach Freigabe des Textes/Konzepts durch Sven dazu.
