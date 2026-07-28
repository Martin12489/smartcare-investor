# smartcare-investor

**Design-Staging-Kopie** der Investoren-Präsentation. Kein Live-Deploy, keine eigene Domain —
dient nur zum lokalen Anschauen/Iterieren von Layout- und Style-Änderungen, bevor sie ins
produktive Repo [`sc-investor-backend`](https://github.com/Martin12489/sc-investor-backend)
übernommen werden (dort als `protected/investor.html`).

## Warum zwei Kopien?

Die eigentliche, live erreichbare Investoren-Seite (**https://smartcarehealth.cloud**) läuft über
ein Node/Express-Backend mit serverseitigem Passwortschutz (siehe README dort). Diese Datei hier
(`smartcare-investor.html`) enthält stattdessen noch die alte, rein clientseitige Passwortabfrage
(Passwörter im Browser-JS sichtbar) — **nicht produktiv nutzen**, nur zum schnellen lokalen
Ansehen im Browser (`file://` oder ein simpler lokaler Server) ohne Backend/Login-Umweg.

## Änderungen synchron halten

Wird hier am Design (Farben, Typografie, Layout) etwas geändert, muss dieselbe Änderung auch in
`sc-investor-backend/protected/investor.html` nachgezogen werden — die beiden Dateien sind
inhaltlich fast identisch (Stand 28.07.2026: Pine/Amber-Farbpalette + Fraunces/Inter/Space-Grotesk,
identisch zu smartcarehealth.de/smartcare-praxen.de), nur der Login-Mechanismus unterscheidet sich.
Am einfachsten: Änderung hier entwickeln/testen, dann denselben Patch im Backend-Repo anwenden
(oder umgekehrt) und beide committen.
