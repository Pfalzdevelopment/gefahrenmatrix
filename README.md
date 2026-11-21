# Gefahrenmatrix

Die **Gefahrenmatrix** ist eine App für iPhone und iPad, mit der Einsatzkräfte Gefahren an der Einsatzstelle schnell per Fingertipp erfassen, ergänzende Notizen festhalten und das Ergebnis als PDF im Format DIN A4 weitergeben können.

Die Matrix folgt dem bekannten Schema der Gefahren der Einsatzstelle (A-C-E-Schema): Atemgifte, Angstreaktion, Ausbreitung, Atomare Strahlung, Chemische Stoffe, Erkrankung/Verletzung, Explosion, Elektrizität und Einsturz.

## Funktionen

- **Matrix zum Anklicken:** Felder durch Antippen markieren und wieder abwählen.
  - Oben wird festgehalten, welche Gefahren erkannt sind (A, C, E).
  - Darunter wird festgehalten, welche Gefahren für Menschen, Tiere, Umwelt und Sachwerte abgewehrt werden müssen und wovor sich die Einsatzkräfte (Mannschaft) schützen müssen.
- **Gesperrte Felder:** Felder, in denen nichts eingetragen werden kann, sind dunkelrot schraffiert und lassen sich nicht antippen.
- **Freie Zeilen:** Einzelne Zeilen können selbst beschriftet werden.
- **Einsatzstichwort:** Ein eigenes Feld oberhalb der Matrix. Das Stichwort erscheint als Überschrift im PDF.
- **Notizzettel:** Mit einem Umschalter wechseln Sie zwischen Matrix und einem Notizzettel für freien Text.
- **PDF-Export im Format DIN A4:**
  - Seite 1 enthält Überschrift, Matrix und, falls vorhanden, den Beginn der Notizen.
  - Längere Notizen laufen automatisch auf weitere DIN-A4-Seiten.
  - Jede Seite trägt die Seitenzahl („Seite X von Y“).
  - Der Notizzettel erscheint nur im PDF, wenn etwas eingetragen wurde.
  - Der Dateiname enthält Stichwort und Datum.
- **Vorschau, Teilen und Sichern:** Das fertige PDF lässt sich in der App ansehen, mit anderen Apps teilen (AirDrop, Mail, Nachrichten usw.) und in der Dateien-App speichern.
- **Automatisches Speichern:** Alle Eingaben bleiben beim Schließen der App erhalten.
- **Zurücksetzen:** Mit einem Fingertipp werden Markierungen, Beschriftungen, Stichwort und Notizen gelöscht.
- **Rotes Farbschema:** Gut lesbar und unabhängig von der Hell/Dunkel-Einstellung des Geräts.

## Datenschutz

Die App erhebt, speichert und übermittelt keine personenbezogenen Daten. Alle Eingaben bleiben lokal auf dem Gerät. Es gibt keine Nutzerkonten, keine Werbung und keine Tracking- oder Analysedienste. Details siehe [Datenschutzerklärung](datenschutz.md).

## Technik

- Entwickelt mit **SwiftUI** (Swift), Zielplattformen iPhone und iPad.
- Speicherung der Eingaben lokal über `UserDefaults`.
- PDF-Erzeugung mit `ImageRenderer` und Core Graphics, Seitenumbruch der Notizen mit Core Text.
- Vorschau mit PDFKit, Teilen mit `ShareLink`, Sichern mit `fileExporter`.
- Der gesamte Code liegt in einer Datei: `GefahrenmatrixApp.swift`.

## Projekt einrichten

1. In Xcode ein neues iOS-Projekt (App, Oberfläche SwiftUI) anlegen.
2. Die automatisch erzeugten Swift-Dateien löschen und `GefahrenmatrixApp.swift` hinzufügen.
3. Unter *Supported Destinations* iPhone und iPad aktivieren.
4. Das App-Icon im Asset-Katalog unter `AppIcon` hinterlegen.
5. Unter *Signing & Capabilities* ein Team und eine eigene Bundle-ID einstellen.
6. Gerät oder Simulator wählen und mit ⌘R starten.

## Support

Fragen, Fehler oder Anregungen: siehe [Support](support.md).

## Hinweis

Die App ist ein Hilfsmittel und ersetzt nicht die Lagebeurteilung durch die Einsatzkräfte.
