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

- Farben orientiert an [[00 Kontext/Fairbeamtet/Branding.md|Branding]]: Blau dominant, Pink/Magenta als Akzent, weißer Text auf dunklem Grund. Da dort keine exakten Hex-Werte hinterlegt sind, erstmal Platzhalter-Töne gesetzt (`#1B4F8C` Blau, `#E6007E` Pink/Magenta, `#0F1E33` Dunkelgrund) – **vor Go-Live gegen die echten Marken-Hex-Werte von der Website tauschen**.
- Kein Gender-Toggle (anders als bei der Marketingmieze-Version) – die BMI-Formel selbst ist geschlechtsneutral, und die recherchierten PKV-Schwellenwerte unterscheiden nicht nach Geschlecht.
- Gauge-Segmente bewusst an der PKV-Logik ausgerichtet, nicht nur an den WHO-Kategorien: "Übergewicht" endet bei BMI 30, genau an der Schwelle, ab der laut Recherche so gut wie alle Versicherer einen Zuschlag ansetzen. Die Farbe kippt an dieser Stelle von Blau auf Pink/Magenta (Signalfarbe für "jetzt handeln/anonym anfragen").
- CTA-Button führt zur anonymen Risikovoranfrage (Platzhalter-Link `#`, echte URL noch einsetzen), nicht zu einem generischen Kontaktformular.

## Nächste Schritte

- [x] Code-Entwurf (Layout) erstellt
- [ ] Echte Marken-Hex-Werte von fairbeamtet.de einsetzen (aktuell Platzhalter)
- [ ] Echten Link zur Risikovoranfrage-Seite einsetzen
- [ ] Sven zur fachlichen Prüfung vorlegen (Zahlen, Schwellenwerte, Rechtssicherheit, Texte)
- [ ] Erst nach Freigabe: Mascot-Visual erstellen (Branding: Funko-Pop-Style "Sven"-Maskottchen)
- [ ] Erst nach Freigabe: live schalten

## Code

Entwurf, noch nicht fachlich geprüft. Layout fokussiert, Texte können sich noch ändern.

```html
<div class="fb-bmi-rechner">
  <div class="fb-bmi-hero">
    <h1>BMI-Rechner: Was dein Gewicht für deine PKV bedeutet</h1>
    <p class="fb-bmi-intro">Du willst wissen, ob dein Gewicht beim PKV-Abschluss zum Problem wird? Dein BMI ist der erste Wert, den jeder Versicherer bei der Gesundheitsprüfung ansieht. Rechne ihn hier aus. Dann zeig ich dir, was die Zahl für dich bedeutet.</p>
  </div>

  <div class="fb-bmi-mythos">
    <p>&bdquo;Ein hoher BMI bedeutet immer eine Ablehnung.&ldquo;</p>
    <p>Bis BMI 30 verlangt praktisch kein Versicherer einen Zuschlag wegen des Gewichts allein. Erst danach wird es ernst.</p>
  </div>

  <div class="fb-bmi-grid">
    <div class="fb-bmi-form-card">
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

    <div class="fb-bmi-cta">
      <p>Willst du wissen, was dein BMI bei einem konkreten Versicherer tatsächlich bedeutet? Dann frag ich das für dich anonym an. Du bekommst eine echte Antwort, ohne dass irgendwo dein Name auftaucht und ohne dass du dich festlegst.</p>
      <a href="#" class="fb-bmi-cta-button">Meine Chancen anonym klären lassen</a>
    </div>
  </div>
</div>

<style>
.fb-bmi-rechner {
  max-width: 1100px;
  margin: 0 auto;
  padding: 48px 24px;
  font-family: 'Inter', sans-serif;
  color: #0F1E33;
}
.fb-bmi-hero {
  background: #0F1E33;
  color: #fff;
  border-radius: 20px;
  padding: 56px 40px;
  margin-bottom: 32px;
  text-align: center;
}
.fb-bmi-hero h1 {
  font-size: clamp(1.8rem, 4vw, 2.8rem);
  margin: 0 0 16px 0;
  line-height: 1.15;
}
.fb-bmi-intro {
  max-width: 640px;
  margin: 0 auto;
  font-size: 1.1rem;
  line-height: 1.6;
  color: rgba(255,255,255,0.9);
}

.fb-bmi-mythos {
  border-left: 4px solid #E6007E;
  background: #F4F6FA;
  padding: 20px 24px;
  margin-bottom: 32px;
  border-radius: 0 12px 12px 0;
}
.fb-bmi-mythos p:first-child {
  font-weight: 700;
  font-style: italic;
  margin: 0 0 8px 0;
}
.fb-bmi-mythos p:last-child {
  margin: 0;
  line-height: 1.6;
}

.fb-bmi-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 28px;
  align-items: start;
  margin-bottom: 32px;
}
@media (max-width: 860px) {
  .fb-bmi-grid {
    grid-template-columns: 1fr;
  }
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
  background: #0F1E33;
  color: #fff;
  min-height: 260px;
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
  color: #0F1E33 !important;
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
  border-color: #1B4F8C;
}

.fb-bmi-button {
  font-family: 'Inter', sans-serif;
  background: #1B4F8C;
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
  background: #163f70;
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
  font-size: 3.6rem;
  font-weight: 700;
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
  flex: 0 0 11.67%;
  background: #8FB7E0;
  border-radius: 999px 0 0 999px;
}
.fb-bmi-segment-normal {
  flex: 0 0 21.67%;
  background: #1B4F8C;
}
.fb-bmi-segment-ueber {
  flex: 0 0 16.67%;
  background: #6F4E8C;
}
.fb-bmi-segment-adipositas {
  flex: 0 0 50%;
  background: #E6007E;
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
  box-shadow: 0 0 0 2px #0F1E33;
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
  flex: 0 0 11.67%;
  color: #8FB7E0;
}
.fb-bmi-label-normal {
  flex: 0 0 21.67%;
  color: #6F9BD1;
}
.fb-bmi-label-ueber {
  flex: 0 0 16.67%;
  color: #B08FCB;
}
.fb-bmi-label-adipositas {
  flex: 0 0 50%;
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
  font-size: 1.4rem;
}
.fb-bmi-cta {
  margin-top: 24px;
  padding-top: 24px;
  border-top: 1px solid #D6DCE8;
  text-align: center;
}
.fb-bmi-cta-button {
  display: inline-block;
  margin-top: 16px;
  background: #E6007E;
  color: #fff;
  text-decoration: none;
  border-radius: 999px;
  padding: 14px 28px;
  font-weight: 700;
}
.fb-bmi-cta-button:hover {
  background: #c40069;
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

  function markerPosition(bmi) {
    var min = 15, max = 45;
    var pct = (bmi - min) / (max - min) * 100;
    if (pct < 0) pct = 0;
    if (pct > 100) pct = 100;
    return pct;
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

- Schriftart "Inter" angenommen, siehe Branding-Notiz "klare, moderne serifenlose Schrift" – falls fairbeamtet.de eine andere Schrift nutzt, im Code austauschen.
- Farben sind Platzhalter (siehe Layout-Entscheidungen oben), vor Go-Live gegen echte Marken-Hex-Werte tauschen.
- Kein Mascot/Bild im Code integriert – kommt erst nach Freigabe des Textes/Konzepts durch Sven dazu.
