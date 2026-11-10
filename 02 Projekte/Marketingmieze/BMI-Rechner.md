---
tags: [projekt, marketingmieze]
status: entwurf
erstellt: 2026-11-10
---

# BMI-Rechner (marketingmieze.com)

## Ziel

Ein BMI-Rechner als eigenständiges Tool auf marketingmieze.com, angelehnt an den [EDEKA BMI-Rechner](https://www.edeka.de/wissen/tests-und-rechner/bmi-rechner/), aber im Marketingmieze-Ton statt neutral-sachlich.

Später (zweite Phase, eigenes Vorhaben): fürs fairbeamtet.de-Umfeld adaptieren, im Kontext PKV/Beihilfe-Gesundheitsprüfung. Bis dahin strikt nur für Marketingmieze umsetzen, nicht vermischen.

## Status

Entwurf – Code wurde als fertiger HTML/CSS/JS-Block gebaut, muss noch auf der Seite eingefügt und getestet werden.

## Referenz: Aufbau EDEKA BMI-Rechner

- Eingabefelder: Geschlecht (weiblich/männlich), Alter, Körpergröße (cm), Körpergewicht (kg) → Button "Berechnen"
- Ergebnis: BMI-Zahl + Label "Body-Mass-Index"
- Zwei Infoboxen: Bewertung nach Alter, Bewertung nach Geschlecht
- Formel-Erklärung: Gewicht (kg) ÷ Größe (m)²
- Kategorien: < 18,5 Untergewicht · 18,5–24,9 Normalgewicht · ≥ 25 Übergewicht · ≥ 30 Adipositas
- Abschnitt zu Grenzen des BMI (berücksichtigt keine Muskelmasse/Fettverteilung)

## Entscheidungen (2026-11-10)

- Technische Umsetzung: fertiger HTML/CSS/JS-Code zum Einfügen per "Custom HTML"-Block in Blocksy/Gutenberg, kein Plugin
- Tonalität: Marketingmieze-Stil nach [[00 Kontext/Marketingmieze/Schreibstil.md|Schreibstil]] – BMI-Limitierungen direkt benennen statt neutral wegzulächeln
- Farben/Schrift: passend zum aktuellen Branding (Pink `#D6336C`, Charcoal `#2B2730`, Senfgelb `#FFD166` als Akzent, Headlines in Bricolage Grotesque, Fließtext in Inter)
- Persönliche Geschichte (30 kg Abnahme mit Mounjaro, raus aus dem dreistelligen Bereich, verbesserte Diabetes-Werte) bewusst mit vollem Detailgrad veröffentlicht, inkl. Medikamentenname – als eigener Abschnitt über dem Rechner. Kernbotschaft: Abnehmspritze wirkt nicht ohne Ernährungsumstellung und Sport, entgegen der weitverbreiteten Annahme, es sei der einfache Weg.
- Redesign 2026-11-10: ursprüngliche Version war zu schmal (640px) und wirkte lieblos. Jetzt breiteres Layout (max. 1100px), zweispaltiges Grid (Formular links, Ergebnis-Karte rechts, sticky beim Scrollen), Geschlecht als Pill-Toggle statt Radio-Buttons, Ergebnis mit farbiger BMI-Skala (Gauge) statt nur nackter Zahl.
- Hero-Banner ergänzt 2026-11-10: pinke Box im Stil der Startseite, mit "BMI-Rechner" als großer kursiver Headline, Sternchen-Tagline und "Jetzt berechnen"-Button, der per Anker-Link runter zum Formular springt. Das ist ein Element innerhalb des Seiteninhalts (Custom-HTML-Block) – nicht zu verwechseln mit dem globalen Seiten-Header (Logo/Menü/Dark-Mode-Switch), der theme-seitig ohnehin automatisch auf jeder Seite erscheint.

## Nächste Schritte

- [x] Edeka-Rechner als Referenz analysiert
- [x] Code gebaut (HTML/CSS/JS, siehe unten)
- [ ] Code in eine neue Seite/Unterseite auf marketingmieze.com einfügen (Custom-HTML-Block)
- [ ] Auf Mobile/Desktop testen
- [ ] Später: Variante für fairbeamtet.de (PKV/Beihilfe-Kontext) ableiten

## Code

Fertiger, eigenständiger Block (HTML + CSS + JS in einem) – einfach komplett in einen "Custom HTML"-Block einfügen.

```html
<div class="mm-bmi-rechner">
  <div class="mm-bmi-hero">
    <h1>BMI-Rechner</h1>
    <p class="mm-bmi-hero-tagline">★ Keine Beschönigung ★ Keine Ausreden ★ Nur deine Zahl ★</p>
    <p class="mm-bmi-hero-intro">Der Body-Mass-Index ist kein Urteil über dich als Mensch – nur eine Zahl aus Gewicht und Größe. Trotzdem lügt sie nicht, wenn man sie richtig liest. Trag deine Daten ein, dann siehst du, wo du stehst.</p>
    <a href="#mmBmiStart" class="mm-bmi-hero-button">Jetzt berechnen</a>
  </div>

  <div class="mm-bmi-story" id="mmBmiStart">
    <h3>Warum ich hier überhaupt mitrede</h3>
    <p>Ich hab mit Mounjaro 30 Kilo abgenommen. Ja, genau die Spritze, über die gerade jeder redet. Endlich raus aus dem dreistelligen Kilobereich, und meine Diabetes-Werte haben sich seitdem massiv verbessert.</p>
    <p>Was mich wirklich nervt: wie viele Leute glauben, die Spritze allein macht den Job. Einfach pieksen und zusehen, wie die Kilos purzeln. Bullshit. Ohne Ernährungsumstellung und Sport passiert so gut wie nichts – und ja, Sport gehört dazu, nicht nur weniger essen. Den inneren Schweinehund besiegen ist zum Fick nochmal verdammt schwer, Spritze hin oder her. Die nimmt dir den Hunger, nicht die Arbeit ab.</p>
    <p>Der Rechner hier unten ersetzt keinen Arztbesuch und erst recht keine Diagnose. Er ist einfach der ehrliche Ausgangspunkt, von dem aus ich selbst losgelegt habe – vielleicht ist er das auch für dich.</p>
  </div>

  <div class="mm-bmi-grid">
    <div class="mm-bmi-form-card">
      <form id="mmBmiForm">
        <div class="mm-bmi-gender">
          <input type="radio" id="mmGeschlechtW" name="geschlecht" value="weiblich" class="mm-bmi-radio" checked>
          <label for="mmGeschlechtW" class="mm-bmi-pill">Weiblich</label>
          <input type="radio" id="mmGeschlechtM" name="geschlecht" value="maennlich" class="mm-bmi-radio">
          <label for="mmGeschlechtM" class="mm-bmi-pill">Männlich</label>
        </div>

        <div class="mm-bmi-fields">
          <label class="mm-bmi-field">
            Alter in Jahren
            <input type="number" id="mmAlter" min="1" max="120" required>
          </label>

          <label class="mm-bmi-field">
            Größe in cm
            <input type="number" id="mmGroesse" min="50" max="250" required>
          </label>

          <label class="mm-bmi-field">
            Gewicht in kg
            <input type="number" id="mmGewicht" min="20" max="400" step="0.1" required>
          </label>
        </div>

        <button type="submit" class="mm-bmi-button">Berechnen</button>
      </form>
    </div>

    <div class="mm-bmi-result-card">
      <div class="mm-bmi-placeholder" id="mmBmiPlaceholder">
        <p>Trag links deine Werte ein. Hier erscheint die Wahrheit – ohne Weichspüler.</p>
      </div>

      <div class="mm-bmi-result" id="mmBmiResult" hidden>
        <div class="mm-bmi-number"><span id="mmBmiValue">0</span></div>
        <div class="mm-bmi-kategorie" id="mmBmiKategorie"></div>

        <div class="mm-bmi-gauge">
          <div class="mm-bmi-gauge-track">
            <span class="mm-bmi-segment mm-bmi-segment-unter"></span>
            <span class="mm-bmi-segment mm-bmi-segment-normal"></span>
            <span class="mm-bmi-segment mm-bmi-segment-ueber"></span>
            <span class="mm-bmi-segment mm-bmi-segment-adipositas"></span>
            <div class="mm-bmi-marker" id="mmBmiMarker"></div>
          </div>
          <div class="mm-bmi-gauge-labels">
            <span>Unter</span><span>Normal</span><span>Über</span><span>Adipositas</span>
          </div>
        </div>

        <p class="mm-bmi-kommentar" id="mmBmiKommentar"></p>
      </div>
    </div>
  </div>

  <div class="mm-bmi-infobox">
    <h3>Was die Zahl wirklich bedeutet – und was nicht</h3>
    <p>Der BMI teilt dein Gewicht in Kilogramm durch deine Größe in Metern zum Quadrat. Mehr nicht. Er unterscheidet nicht zwischen Muskeln und Fett, nicht zwischen Bauchfett und Hüftspeck, nicht zwischen "trainiert" und "dünn". Ein Kraftsportler mit wenig Körperfett kann hier als "übergewichtig" durchfallen – weil Muskeln schwerer sind als Fett, nicht weil er ungesund lebt.</p>
    <p>Die Kategorien (grob, für Erwachsene):</p>
    <ul>
      <li>unter 18,5 – Untergewicht</li>
      <li>18,5 bis 24,9 – Normalgewicht</li>
      <li>25 bis 29,9 – Übergewicht</li>
      <li>ab 30 – Adipositas</li>
    </ul>
    <p>Mit dem Alter darf der Wert übrigens steigen – kleine Reserven helfen älteren Körpern, Krankheiten besser wegzustecken. Und zwischen den Geschlechtern unterscheidet sich der "gesunde" Bereich leicht, weil Frauen von Natur aus mehr Körperfett und Männer mehr Muskelmasse haben.</p>
    <p><strong>Kurz gesagt:</strong> Nimm die Zahl als Orientierung, nicht als Urteil. Bei Unsicherheit fragst du besser deinen Arzt statt eine Website im Internet – auch diese hier.</p>
  </div>
</div>

<style>
.mm-bmi-rechner {
  max-width: 1100px;
  margin: 0 auto;
  padding: 48px 24px;
  font-family: 'Inter', sans-serif;
  color: #2B2730;
}
.mm-bmi-hero {
  background: #D6336C;
  color: #fff;
  border-radius: 24px;
  padding: 64px 40px;
  margin-bottom: 40px;
  text-align: center;
}
.mm-bmi-hero h1 {
  font-family: 'Bricolage Grotesque', sans-serif;
  font-style: italic;
  font-weight: 700;
  font-size: clamp(2.6rem, 6vw, 4.5rem);
  margin: 0 0 16px 0;
  line-height: 1;
}
.mm-bmi-hero-tagline {
  font-size: 1rem;
  letter-spacing: 0.05em;
  opacity: 0.9;
  margin-bottom: 20px;
}
.mm-bmi-hero-intro {
  max-width: 560px;
  margin: 0 auto 28px auto;
  font-size: 1.1rem;
  line-height: 1.6;
}
.mm-bmi-hero-button {
  display: inline-block;
  font-family: 'Bricolage Grotesque', sans-serif;
  background: #FFD166;
  color: #2B2730;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 32px;
  font-size: 1.1rem;
  font-weight: 700;
  transition: transform 0.1s ease;
}
.mm-bmi-hero-button:hover {
  transform: scale(1.03);
}
.mm-bmi-rechner h3 {
  font-family: 'Bricolage Grotesque', sans-serif;
  font-size: 1.3rem;
  margin-top: 0;
}
.mm-bmi-story {
  border-left: 4px solid #D6336C;
  background: #FAF7FA;
  padding: 24px 28px;
  margin-bottom: 40px;
  border-radius: 0 16px 16px 0;
  max-width: 820px;
}
.mm-bmi-story p {
  line-height: 1.6;
  margin: 0 0 12px 0;
}
.mm-bmi-story p:last-child {
  margin-bottom: 0;
}

.mm-bmi-grid {
  display: grid;
  grid-template-columns: 1.15fr 0.85fr;
  gap: 32px;
  align-items: start;
  margin-bottom: 40px;
}
@media (max-width: 860px) {
  .mm-bmi-grid {
    grid-template-columns: 1fr;
  }
}

.mm-bmi-form-card,
.mm-bmi-result-card {
  background: #fff;
  border: 1px solid rgba(43,39,48,0.08);
  border-radius: 20px;
  padding: 32px;
  box-shadow: 0 16px 40px rgba(43,39,48,0.08);
}
.mm-bmi-result-card {
  position: sticky;
  top: 24px;
  background: #2B2730;
  color: #fff;
  min-height: 260px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.mm-bmi-gender {
  display: flex;
  gap: 12px;
  margin-bottom: 24px;
}
.mm-bmi-radio {
  position: absolute;
  opacity: 0;
  pointer-events: none;
}
.mm-bmi-pill {
  display: inline-block;
  box-sizing: border-box;
  padding: 10px 22px;
  border-radius: 999px;
  border: 2px solid #ddd;
  color: #2B2730;
  font-size: 0.95rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.15s ease;
}
.mm-bmi-radio:checked + .mm-bmi-pill {
  background: #2B2730;
  border-color: #2B2730;
  color: #fff;
}

.mm-bmi-fields {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-bottom: 24px;
}
@media (max-width: 560px) {
  .mm-bmi-fields {
    grid-template-columns: 1fr;
  }
}
.mm-bmi-field {
  display: flex;
  flex-direction: column;
  gap: 8px;
  font-weight: 600;
  font-size: 1rem;
}
.mm-bmi-field input {
  background: #fff !important;
  color: #2B2730 !important;
  font-family: 'Inter', sans-serif;
  font-size: 1.15rem;
  padding: 16px 18px;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-sizing: border-box;
  width: 100%;
}
.mm-bmi-field input:focus {
  outline: none;
  border-color: #D6336C;
}

.mm-bmi-button {
  font-family: 'Bricolage Grotesque', sans-serif;
  background: #FFD166;
  color: #2B2730;
  border: none;
  border-radius: 999px;
  padding: 16px 28px;
  font-size: 1.1rem;
  font-weight: 700;
  cursor: pointer;
  width: 100%;
  transition: transform 0.1s ease;
}
.mm-bmi-button:hover {
  transform: scale(1.015);
}

.mm-bmi-placeholder {
  text-align: center;
  font-size: 1.05rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.8);
}
.mm-bmi-result {
  text-align: center;
  width: 100%;
}
.mm-bmi-number {
  font-family: 'Bricolage Grotesque', sans-serif;
  font-size: 4rem;
  font-weight: 700;
  line-height: 1;
}
.mm-bmi-kategorie {
  font-size: 1.2rem;
  font-weight: 700;
  margin-top: 8px;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  color: #FFD166;
}
.mm-bmi-gauge {
  margin: 24px 0;
}
.mm-bmi-gauge-track {
  position: relative;
  display: flex;
  height: 12px;
  border-radius: 999px;
  overflow: visible;
}
.mm-bmi-segment {
  display: block;
  height: 100%;
}
.mm-bmi-segment-unter {
  flex: 0 0 14%;
  background: #6FA8DC;
  border-radius: 999px 0 0 999px;
}
.mm-bmi-segment-normal {
  flex: 0 0 26%;
  background: #6BBF8A;
}
.mm-bmi-segment-ueber {
  flex: 0 0 20%;
  background: #FFD166;
}
.mm-bmi-segment-adipositas {
  flex: 0 0 40%;
  background: #D6336C;
  border-radius: 0 999px 999px 0;
}
.mm-bmi-marker {
  position: absolute;
  top: -6px;
  left: 0%;
  width: 4px;
  height: 24px;
  background: #fff;
  border-radius: 2px;
  box-shadow: 0 0 0 2px #2B2730;
  transition: left 0.4s ease;
}
.mm-bmi-gauge-labels {
  display: flex;
  justify-content: space-between;
  font-size: 0.75rem;
  margin-top: 8px;
  color: rgba(255,255,255,0.7);
}
.mm-bmi-kommentar {
  font-size: 1rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.9);
}

.mm-bmi-infobox {
  background: #FAF7FA;
  padding: 32px;
  border-radius: 20px;
  line-height: 1.6;
}
.mm-bmi-infobox ul {
  padding-left: 20px;
}
</style>

<script>
(function() {
  var form = document.getElementById('mmBmiForm');
  var placeholder = document.getElementById('mmBmiPlaceholder');
  var result = document.getElementById('mmBmiResult');
  var valueEl = document.getElementById('mmBmiValue');
  var kategorieEl = document.getElementById('mmBmiKategorie');
  var kommentarEl = document.getElementById('mmBmiKommentar');
  var markerEl = document.getElementById('mmBmiMarker');

  function markerPosition(bmi) {
    var min = 15, max = 40;
    var pct = (bmi - min) / (max - min) * 100;
    if (pct < 0) pct = 0;
    if (pct > 100) pct = 100;
    return pct;
  }

  function kategorisieren(bmi) {
    if (bmi < 18.5) {
      return {
        label: 'Untergewicht',
        text: 'Du liegst unter dem, was gemeinhin als Normalgewicht gilt. Kein Drama, aber auch kein Grund, es zu ignorieren – vor allem, wenn das ungewollt passiert ist.'
      };
    } else if (bmi < 25) {
      return {
        label: 'Normalgewicht',
        text: 'Rein rechnerisch bist du im grünen Bereich. Was das über deine tatsächliche Gesundheit aussagt, ist eine andere Geschichte – Ernährung, Bewegung und Schlaf zählen mindestens genauso.'
      };
    } else if (bmi < 30) {
      return {
        label: 'Übergewicht',
        text: 'Die Zahl sagt "Übergewicht". Ob das für dich persönlich relevant ist, hängt von mehr ab als dieser einen Formel – Muskelanteil, Lebensstil, Fettverteilung. Trotzdem: ein Wert, den man nicht einfach wegwischen sollte.'
      };
    } else {
      return {
        label: 'Adipositas',
        text: 'Hier wird es ernst genug, um nicht wegzuschauen. Das heißt nicht, dass du versagt hast – aber es lohnt sich, das Thema aktiv anzugehen, am besten mit ärztlicher Unterstützung statt allein mit dieser Website.'
      };
    }
  }

  form.addEventListener('submit', function(e) {
    e.preventDefault();
    var groesseCm = parseFloat(document.getElementById('mmGroesse').value);
    var gewichtKg = parseFloat(document.getElementById('mmGewicht').value);

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

- Google Fonts "Bricolage Grotesque" und "Inter" müssen auf der Seite geladen sein (sind es vermutlich schon über die Theme-Einstellungen aus dem Branding-Update).
- Farben sind fest auf die aktuelle Marketingmieze-Palette gesetzt (Pink `#D6336C`, Charcoal `#2B2730`, Senfgelb `#FFD166`). Bei späteren Farbänderungen am Branding müssen die Hex-Werte hier manuell nachgezogen werden.
- Geschlecht wird aktuell nur erfasst, aber nicht in die Formel eingerechnet (wie beim Original – die Kategorien unterscheiden sich im Rechenweg nicht, nur im Infotext wird auf den Unterschied hingewiesen).
