# Light RP Kalender

Vorabversion für einen kleinen Testkreis. Zeigt öffentliche RP-Termine aus dem FF14-Light Wiki für heute, diese und nächste Woche. Mit Suche, Adresskopie, externen Eventlinks und optionaler Lifestream-Reisehilfe.

## Installation über Dalamud

Unter `/xlsettings` → **Experimentell** → **Custom Plugin Repositories / Benutzerdefinierte Plugin-Repositories** diese URL hinzufügen, mit **+** übernehmen und speichern:

```text
https://raw.githubusercontent.com/RolandBergensjn/LightRPKalender/main/pluginmaster.json
```

Danach `/xlplugins` öffnen, die Liste gegebenenfalls aktualisieren und **Light RP Kalender** installieren. Eine bisherige Dev-Version vorher deaktivieren und deren **Dev Plugin Location** entfernen. Kalender mit `/lightkalender` öffnen, Einstellungen mit `/lightkalender config`.

## Bedienung und Voraussetzungen

- Heute / Diese Woche / Nächste Woche; Suche über beide Wochen. Startansicht einstellbar, Standard Heute.
- Kopierbare Adressen, wahlweise kurz oder ausgeschrieben.
- Externe Eventlinks, einschließlich Carrd-Beschriftung.
- Anzeige der verbliebenen Öffnungszeit und Hinweise auf Wartungen.
- Wochenansichten mit Kalenderwoche; Datenstand mit Datum, Uhrzeit und Zeitzone.
- Drei gespeicherte Teleport-Modi: Kommando kopieren (Standard), direkte Bezirksreise nach zwei Klicks mit 5-Sekunden-Bestätigung oder nach einem Klick.
- Teleporthilfe optional: benötigt Lifestream **2.5.4.4**. Ohne installiertes Lifestream bleiben dessen Buttons verborgen. Direkte Reisen benötigen eine geladene Lifestream-Instanz; keine Lifestream-Dateien werden mitgeliefert.
- Gebaut für Dalamud **API 15**, .NET 10 / Windows x64.

Die Reisehilfe verwendet das in Lifestream 2.5.4.4 statisch untersuchte Grundstück-0-Verhalten und endet am Wohnbezirk, nicht am Haus oder gezielt in der Erweiterung. Dieses Verhalten ist undokumentiert und versionsabhängig. Die Anreise und mögliche Bewegung organisiert Lifestream. Kopieren ist der Standard; direkte Reisen erfolgen erst nach entsprechender Einstellung und bewussten Klicks.

Dies ist ein benutzerdefiniertes Repository, keine Aufnahme in das offizielle Dalamud-Pluginverzeichnis. Ein öffentliches GitHub-Repository und seine Downloads sind für jeden abrufbar; die Beschränkung auf einen Testkreis ist organisatorisch, keine technische Zugriffssperre.

## Test-Rückmeldungen

Bitte Plugin-/Dalamud-/Lifestream-Version, betroffenen Termin, erwartetes und tatsächliches Verhalten sowie bei Bedarf einen zugeschnittenen Screenshot angeben. Keine Zugangsdaten oder vollständigen privaten Logs veröffentlichen.

## Kalenderquelle

[FF14-Light Wiki](https://ff14-light.fandom.com/de/wiki/Kategorie:Eventkalender), Inhalte nach [Fandom-Lizenzhinweisen](https://www.fandom.com/de/licensing-de) / CC BY-SA. Öffentlicher API-Abruf ohne Wiki-Login. Eventseiten werden erst nach Klick im normalen Browser geöffnet. Dies ist keine offizielle Anwendung von Square Enix oder den Wiki-Betreibern.
