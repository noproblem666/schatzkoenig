# Wer wird Schatzkönig? – PWA

Eine lokale GPS-Quiz-Schnitzeljagd für iPhone (Safari / Zum Home-Bildschirm).

## Veröffentlichung mit GitHub Pages

1. Auf GitHub ein neues Repository anlegen, z. B. `schatzkoenig`.
2. Alle Dateien aus diesem Ordner in das Repository hochladen (Dateien müssen direkt im Repository-Hauptverzeichnis liegen).
3. Im Repository **Settings → Pages** öffnen.
4. Unter **Build and deployment** `Deploy from a branch` wählen, Branch `main`, Ordner `/ (root)`, anschließend **Save**.
5. Nach der Veröffentlichung die angezeigte `https://...github.io/.../`-Adresse auf dem iPhone in Safari öffnen.
6. In Safari auf **Teilen → Zum Home-Bildschirm** tippen.
7. Beim ersten Start Standortzugriff erlauben.

## Spiel einrichten

- Elternbereich öffnen.
- Für jede Station über **Meine Position übernehmen** den Standort vor Ort speichern. Alternativ Breiten- und Längengrad eintragen.
- Radius pro Station einstellen (Standard 10 m; im Wald ggf. 15–25 m).
- Eine Katalogfrage auswählen oder eine eigene Frage mit vier Antworten, richtiger Lösung und Erklärung eintragen.
- Speichern und das Abenteuer starten.

## Hinweise / Grenzen

- GPS funktioniert nur zuverlässig mit HTTPS und erteilter Standortfreigabe. iOS kann die Genauigkeit unter Bäumen stark verschlechtern. Die App muss während der Schatzsuche geöffnet und im Vordergrund bleiben.
- Die Eltern können eine Station während des Spiels manuell freigeben, indem sie den Elternbereich öffnen und bei der betreffenden Station auf **Station manuell freigeben** tippen.
- Die Karte lädt Leaflet und OpenStreetMap-Kartenkacheln aus dem Internet. Karten sind daher nicht offline verfügbar. Die OpenStreetMap-Urheberangabe wird auf der Karte angezeigt; bitte die Nutzungsrichtlinien des öffentlichen Tile-Servers beachten.
- Quiz, Stationen und Spielstand werden im lokalen Browser-Speicher auf diesem iPhone abgelegt. Browserdaten nicht löschen, solange die Konfiguration benötigt wird.
- Dies ist ein erster funktionsfähiger Prototyp. Vor dem Kindergeburtstag unbedingt die komplette Route vor Ort testen.
