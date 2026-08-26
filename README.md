# BeGuNa – Themen sichern

Mobile Website zur täglichen Verteilung von Themen. Das Backoffice verwendet
einen gemeinsamen, über Firebase Authentication geschützten Passwortzugang.

## Enthalten

- `index.html` – komplette Website inklusive Firebase-Konfiguration
- `firestore.rules` – Sicherheitsregeln für die Datenbank

## Einmalige Firebase-Einrichtung

1. In Firebase **Firestore → Regeln** öffnen.
2. Den gesamten Inhalt dort durch den Inhalt von `firestore.rules` ersetzen.
3. **Veröffentlichen** wählen.
4. Unter **Authentication → Nutzer** muss der Nutzer
   `team@backstage-beguna.app` vorhanden sein.

## Bedienung

1. Website öffnen und unten **Backoffice** wählen.
2. Gemeinsames Passwort eingeben.
3. Titel, Zeitraum/Frist und Sprechtext eintragen.
4. Laden und Adresse sind optional.
5. **Thema hinzufügen** wählen.

Besucher tragen bei einem freien Thema nur ihren Namen ein. Die Reservierung
wird als Transaktion gespeichert, damit ein Thema nicht gleichzeitig doppelt
vergeben werden kann.

## Veröffentlichung über GitHub Pages

Die Datei `index.html` muss im Hauptordner des Repositorys liegen. Danach in
GitHub unter **Settings → Pages** als Quelle **Deploy from a branch**, Branch
**main** und Ordner **/(root)** auswählen.
