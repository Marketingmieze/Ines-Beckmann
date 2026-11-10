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
  <h2>Dein BMI. Keine Ausreden, keine Beschönigung.</h2>
  <p class="mm-bmi-intro">Der Body-Mass-Index ist kein Urteil über dich als Mensch – nur eine Zahl aus Gewicht und Größe. Trotzdem lügt sie nicht, wenn man sie richtig liest. Trag deine Daten ein, dann siehst du, wo du stehst.</p>

  <form class="mm-bmi-form" id="mmBmiForm">
    <fieldset>
      <legend>Geschlecht</legend>
      <label><input type="radio" name="geschlecht" value="weiblich" checked> Weiblich</label>
      <label><input type="radio" name="geschlecht" value="maennlich"> Männlich</label>
    </fieldset>

    <label class="mm-bmi-field">
      Alter in Jahren
      <input type="number" id="mmAlter" min="1" max="120" required>
    </label>

    <label class="mm-bmi-field">
      Körpergröße in cm
      <input type="number" id="mmGroesse" min="50" max="250" required>
    </label>

    <label class="mm-bmi-field">
      Körpergewicht in kg
      <input type="number" id="mmGewicht" min="20" max="400" step="0.1" required>
    </label>

    <button type="submit" class="mm-bmi-button">Berechnen</button>
  </form>

  <div class="mm-bmi-result" id="mmBmiResult" hidden>
    <div class="mm-bmi-number"><span id="mmBmiValue">0</span></div>
    <div class="mm-bmi-kategorie" id="mmBmiKategorie"></div>
    <p class="mm-bmi-kommentar" id="mmBmiKommentar"></p>
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
  max-width: 640px;
  margin: 0 auto;
  padding: 32px 24px;
  font-family: 'Inter', sans-serif;
  color: #2B2730;
}
.mm-bmi-rechner h2 {
  font-family: 'Bricolage Grotesque', sans-serif;
  font-size: 2rem;
  color: #2B2730;
  margin-bottom: 8px;
}
.mm-bmi-rechner h3 {
  font-family: 'Bricolage Grotesque', sans-serif;
  font-size: 1.3rem;
  margin-top: 0;
}
.mm-bmi-intro {
  margin-bottom: 24px;
  line-height: 1.5;
}
.mm-bmi-form {
  display: flex;
  flex-direction: column;
  gap: 16px;
  background: #FAF7FA;
  padding: 24px;
  border-radius: 12px;
  margin-bottom: 24px;
}
.mm-bmi-form fieldset {
  border: none;
  padding: 0;
  margin: 0;
  display: flex;
  gap: 24px;
}
.mm-bmi-form fieldset legend {
  font-weight: 600;
  margin-bottom: 8px;
  width: 100%;
}
.mm-bmi-field {
  display: flex;
  flex-direction: column;
  gap: 4px;
  font-weight: 600;
}
.mm-bmi-field input {
  font-family: 'Inter', sans-serif;
  font-size: 1rem;
  padding: 10px 12px;
  border: 1px solid #ccc;
  border-radius: 8px;
}
.mm-bmi-button {
  font-family: 'Bricolage Grotesque', sans-serif;
  background: #FFD166;
  color: #2B2730;
  border: none;
  border-radius: 999px;
  padding: 14px 24px;
  font-size: 1.1rem;
  font-weight: 700;
  cursor: pointer;
  transition: transform 0.1s ease;
}
.mm-bmi-button:hover {
  transform: scale(1.02);
}
.mm-bmi-result {
  text-align: center;
  background: #D6336C;
  color: #fff;
  padding: 32px 24px;
  border-radius: 12px;
  margin-bottom: 24px;
}
.mm-bmi-number {
  font-family: 'Bricolage Grotesque', sans-serif;
  font-size: 3.5rem;
  font-weight: 700;
  line-height: 1;
}
.mm-bmi-kategorie {
  font-size: 1.2rem;
  font-weight: 700;
  margin-top: 8px;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
.mm-bmi-kommentar {
  margin-top: 12px;
  font-size: 1rem;
  line-height: 1.5;
}
.mm-bmi-infobox {
  background: #2B2730;
  color: #fff;
  padding: 24px;
  border-radius: 12px;
  line-height: 1.6;
}
.mm-bmi-infobox ul {
  padding-left: 20px;
}
</style>

<script>
(function() {
  var form = document.getElementById('mmBmiForm');
  var result = document.getElementById('mmBmiResult');
  var valueEl = document.getElementById('mmBmiValue');
  var kategorieEl = document.getElementById('mmBmiKategorie');
  var kommentarEl = document.getElementById('mmBmiKommentar');

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
    result.hidden = false;
    result.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
  });
})();
</script>
```

## Hinweise zur Einbindung

- Google Fonts "Bricolage Grotesque" und "Inter" müssen auf der Seite geladen sein (sind es vermutlich schon über die Theme-Einstellungen aus dem Branding-Update).
- Farben sind fest auf die aktuelle Marketingmieze-Palette gesetzt (Pink `#D6336C`, Charcoal `#2B2730`, Senfgelb `#FFD166`). Bei späteren Farbänderungen am Branding müssen die Hex-Werte hier manuell nachgezogen werden.
- Geschlecht wird aktuell nur erfasst, aber nicht in die Formel eingerechnet (wie beim Original – die Kategorien unterscheiden sich im Rechenweg nicht, nur im Infotext wird auf den Unterschied hingewiesen).
