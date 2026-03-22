# 🌿 Waermekosten-Rechner -- Oekosiedlung Friedrichsdorf

Dieses Tool berechnet die jaehrlichen Waermekosten fuer Haeuser in der Oekosiedlung Friedrichsdorf, die einen Waermelieferungsvertrag mit der ECOenergy Friedrichsdorf GmbH haben. Es setzt die Preisanpassungsformeln aus Paragraph 5 Abs. 2 und 3 des Vertrags (Tarife P-WAe-GP4-122-0001 / P-WAe-AP-101-0013) um.


## 🧮 Wofuer ist der Rechner gedacht?

Mit dem Rechner kannst du deine eigene Waermeabrechnung nachpruefen. Die Berechnung besteht aus zwei Teilen:

- **Grundpreis (Paragraph 5 Abs. 2):** Ein fester Jahresbetrag, der sich einmal jaehrlich zum 1. Januar anpasst. Er haengt von der Anschlussleistung (bei uns 7 kW) und zwei oeffentlichen Destatis-Indizes ab.
- **Arbeitspreis (Paragraph 5 Abs. 3):** Der verbrauchsabhaengige Teil, aufgeteilt in zwei Halbjahre (H1: Januar bis Juni, H2: Juli bis Dezember). Er wird von Erdgas- und Strom-Beschaffungskosten sowie zwei weiteren Destatis-Indizes bestimmt.

Alle Eingabewerte ausser dem individuellen Verbrauch sind fuer saemtliche Haeuser in der Siedlung identisch. Du musst nur deinen eigenen Verbrauch eintragen.


## 🚀 Bedienung in drei Schritten

### 1️⃣ Basisdaten laden

Klicke auf "Basisdaten 2025" (oder "Basisdaten 2024", wenn du das Vorjahr pruefen willst). Damit werden alle gemeinsamen Werte automatisch eingetragen: Anschlussleistung, Destatis-Indizes, ECOenergy-Beschaffungskosten und Mehrwertsteuersaetze.

### 2️⃣ Eigenen Verbrauch eintragen

Trage deinen individuellen Verbrauch fuer beide Halbjahre ein. Diese beiden Felder sind als Pflichtfelder markiert:

- **Verbrauch H1** (Januar bis Juni) in kWh
- **Verbrauch H2** (Juli bis Dezember) in kWh

Die Werte findest du auf Seite 2 deiner Abrechnung in der Tabelle "Betragsberechnung", Spalte "Menge".

### 3️⃣ Berechnung starten

Klicke auf "Jahreskosten berechnen". Das Ergebnis erscheint direkt darunter.


## ⚠️ Wichtig: kWh, nicht MWh

Die Abrechnung zeigt den Verbrauch in MWh (z.B. "3,500 MWh"). Im Rechner gibst du den Wert in kWh ein, also multipliziert mit 1000. Aus 3,500 MWh werden 3500 kWh.

Dezimalwerte kannst du mit Komma oder Punkt eingeben (0,08916 oder 0.08916 -- beides funktioniert).


## 🎨 Was die Eingabefelder bedeuten

Die Felder sind farblich gekennzeichnet:

- 🔵 **Blau -- Oeffentliche Destatis-Indizes:** Frei zugaengliche Statistikwerte vom Statistischen Bundesamt. Koennen unabhaengig ueberprueft werden. Links zu den GENESIS-Tabellen sind im Rechner hinterlegt.
- 🟠 **Orange -- ECOenergy-interne Werte:** Beschaffungskosten fuer Erdgas (B) und Strom (S), die ECOenergy angibt. Nicht unabhaengig pruefbar.
- 🟢 **Gruen -- Eigene Eingabe:** Werte, die du selbst eintraegst (vor allem dein Verbrauch).
- 🟣 **Violett -- Automatisch berechnet:** Vom Rechner ermittelte Zwischenergebnisse, z.B. der GP0-Basiswert oder die Arbeitspreise pro Halbjahr.


## 📊 Was das Ergebnis zeigt

Nach der Berechnung siehst du:

- 💰 **Grundpreis** (netto und brutto pro Jahr)
- ⚡ **Arbeitspreis und Arbeitskosten** fuer jedes Halbjahr einzeln
- 🧾 **Jahresbetrag brutto** -- die Gesamtsumme
- 📅 **Monatlicher Abschlag** (Jahresbetrag geteilt durch 12)
- 🌡️ **Gesamtverbrauch** in MWh und kWh
- 📈 **Effektive Kosten pro kWh** (brutto)

Ausserdem prueft der Rechner zwei Dinge automatisch:

- ✅ **Abgleich mit Basisdaten:** Stimmen der berechnete Grundpreis und die Arbeitspreise mit den hinterlegten Referenzwerten ueberein? Damit laesst sich feststellen, ob die Formeln korrekt angewendet wurden.
- 🔍 **Plausibilitaetspruefung B vs. GG-Index:** Entwickeln sich die internen Erdgas-Beschaffungskosten (B) von ECOenergy im Einklang mit dem oeffentlichen Erdgas-Index (GG)? Starke Abweichungen koennen auf Erklaerungsbedarf hinweisen.


## ⚙️ Technische Hinweise

Der Rechner ist eine einzelne HTML-Datei ohne externe Abhaengigkeiten (ausser Google Fonts). 🌐 Er laeuft komplett im Browser -- es werden keine Daten uebertragen oder gespeichert. 📁 Einfach die Datei `index.html` im Browser oeffnen.
