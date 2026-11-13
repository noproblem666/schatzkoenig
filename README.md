# Mattis große Schnitzeljagd – Wer wird Schatzkönig?

Eine lokale GPS-Quiz-Schnitzeljagd als Progressive Web App (PWA) für iPhone und Safari. Die Kinder folgen einer Schatzroute, beantworten Quizfragen und suchen am Ende die versteckte Schatztruhe.

## Funktionen

- GPS-gestützte Schnitzeljagd mit mehreren Stationen und individuell einstellbarem Ankunftsradius.
- Vollbildkarte mit nächstem Ziel, Entfernung und GPS-Genauigkeit.
- Eine Quizfrage pro Station mit vier Antwortmöglichkeiten (A–D), einer richtigen Antwort und einer kindgerechten Erklärung.
- Automatische Nummerierung der Fragen („Frage 1“, „Frage 2“ usw.).
- Drei gemeinsame Leben und ein 50:50-Joker.
- Nach einer richtigen Antwort wird die Erklärung gezeigt. Erst nach Tippen auf „Weiter“ wird die nächste Station freigegeben.
- Feierliche Animation und Klangsignale bei richtigen Antworten und beim Finale.
- Elternbereich zum Erstellen und Bearbeiten von Stationen, GPS-Koordinaten, Radien und Fragen.
- Schatzgebiet für das Finale: Im Elternbereich lässt sich der Mittelpunkt per GPS oder durch Tippen auf die Karte festlegen. Der Suchradius beträgt wahlweise 50 oder 100 Meter.
- Auf der Abschlussseite sehen die Kinder eine Karte mit dem goldenen Suchkreis, ihrem eigenen GPS-Standort und der ungefähren Entfernung zum Suchgebiet.
- Fragenkatalog mit allgemeinen Quizfragen sowie **30 zusätzlichen Berlin-Fragen**: 15 mittlere und 15 schwere Fragen, unter anderem zu Fernsehturm, Bezirken, Brandenburger Tor, Berliner Mauer, East Side Gallery und Müggelsee.
- Einstellungen, Fragen und Spielstand werden lokal auf dem Gerät gespeichert; für den Ein-Geräte-Betrieb ist kein Benutzerkonto und kein eigener Server erforderlich.

## Elternbereich und PIN

- Beim ersten Öffnen des Elternbereichs wird eine eigene sechsstellige PIN festgelegt und bestätigt.
- Bei jedem weiteren Öffnen wird die PIN abgefragt.
- Nach zwei Minuten Inaktivität wird der Elternbereich automatisch gesperrt.
- Die PIN kann im Elternbereich geändert werden.
- Der Kinder-Spielbereich ist nicht PIN-geschützt.
- Die PIN wird als SHA-256-Hash im lokalen Speicher abgelegt, nicht im Klartext.

**Sicherheitshinweis:** Da die App als statische Website über GitHub Pages läuft, ist die PIN nur ein Schutz gegen versehentliches Öffnen. Sie ist keine echte serverseitige Zugriffssicherung; technisch versierte Personen können lokale Daten oder den Programmcode untersuchen und verändern.

## Spiel einrichten

1. App öffnen und den Elternbereich aufrufen.
2. Für jede Station einen Namen, GPS-Standort und Ankunftsradius festlegen. Den Standort vor Ort per **Meine Position übernehmen** speichern oder Koordinaten im Format `(52.520008, 13.404954)` einfügen.
3. Eine Katalogfrage auswählen oder eine eigene Frage mit vier Antwortmöglichkeiten, richtiger Lösung und Erklärung eintragen.
4. Im Abschnitt **Standort der Schatztruhe** den Mittelpunkt der Schatzsuche per GPS oder durch Tippen auf die Karte festlegen.
5. Für das Schatzgebiet einen Radius von **50 oder 100 Metern** wählen.
6. **Einstellungen speichern** und das Abenteuer starten.

Ein vollständiger Spielstart ist erst möglich, wenn alle Stationen und der Schatzstandort gültige Koordinaten haben.

## Veröffentlichung mit GitHub Pages

1. Repository auf GitHub öffnen.
2. Unter **Settings → Pages** bei **Build and deployment** die Option **Deploy from a branch** wählen.
3. Branch `main` und Ordner `/(root)` auswählen und speichern.
4. Die veröffentlichte GitHub-Pages-Adresse auf dem iPhone in Safari öffnen.
5. In Safari auf **Teilen → Zum Home-Bildschirm** tippen.
6. Beim ersten Start den Standortzugriff erlauben.

## Aktualisieren der App

Die App verwendet einen Service Worker, der die App-Dateien zwischenspeichert. Nach Änderungen wird die Cache-Version in `sw.js` erhöht. Zum Laden der neuesten Version die Website einmal in Safari öffnen und neu laden; danach kann die Home-Bildschirm-App neu gestartet werden.

## Hinweise und Grenzen

- GPS funktioniert nur über HTTPS und mit erteilter Standortfreigabe. Unter Bäumen und im Wald kann die Genauigkeit deutlich schlechter sein. Die App sollte während der Schatzsuche geöffnet und im Vordergrund bleiben.
- Die GPS-Genauigkeit wird angezeigt. Bei Problemen kann ein Elternteil eine Station im Elternbereich manuell freigeben.
- Der Standort der Schatztruhe markiert den **Mittelpunkt des Suchgebiets**, nicht den exakten Versteckort. Die Schatztruhe muss innerhalb des angezeigten Kreises versteckt werden.
- Die Karte nutzt Leaflet und OpenStreetMap-Kartenkacheln. Karten sind nicht offline verfügbar. Die OpenStreetMap-Urheberangabe wird auf der Karte angezeigt; bitte die Nutzungsrichtlinien des öffentlichen Tile-Servers beachten.
- Quizfragen, Stationen, PIN-Hash und Spielstand werden im lokalen Browser-Speicher dieses Geräts abgelegt. Beim Löschen der Safari-Websitedaten können diese Daten verloren gehen.
- Vor dem Einsatz mit Kindern die gesamte Route einschließlich GPS-Empfang, Ankunftsradius, Schatzgebiet und Audio auf dem tatsächlichen iPhone testen.
