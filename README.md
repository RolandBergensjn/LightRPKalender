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
- Neutrale Eventboxen mit grauer Eventart, hervorgehobener Adresse, Stern rechts vom Namen und Kopieren direkt an der Adresse.
- Horizontales Layout mit Zeitbalken unten, Restzeit und quadratischen Browser-/Anreisebuttons. Aufgeklappte Details nutzen die ganze innere Kartenbreite.
- Sanft grüner Restzeitbalken ohne großflächigen grünen Hintergrund. Lila Teleportbutton mit passenden Hover-Farben.
- Dichteres Punktgitter mit kleineren Punkten, örtlicher Maus-Aufhellung und Wellen ausschließlich aus größer und heller werdenden Punkten. Eigene Effekte für Teleport, Website, Vormerken/Entfernen, Kopieren und Details. Kurzer grüner Minutenimpuls am laufenden Zeitbalken. Gemeinsam unter Einstellungen → Punktgitter und Animationen abschaltbar.
- Langsamere Punktwellen mit stärkerem Größenimpuls. Details klappen sofort auf oder zu; direkt danach beginnt die Welle mit der neuen Boxgröße. Öffnen ab Höhe der Zeile Hinweise / Details nach unten; Schließen vom unteren Rand der bereits eingeklappten Box bis leicht über diese Zeile.
- Die Schließwelle ist kürzer; animierte Punkte sind nochmals zehn Prozent größer. Zwei-Klick-Teleport: erster Klick mit gehaltenem, leicht waberndem und scheinbar rotierendem Punktering am Button, zweiter Klick mit Freigabewelle und zwei Folgeimpulsen. Ohne Bestätigung löst sich der Ring nach fünf Sekunden auf. Die Darstellung verlängert die Reisebestätigung nicht.
- Kopierbare Adressen, wahlweise kurz oder ausgeschrieben.
- Externe Eventlinks, einschließlich Carrd-Beschriftung.
- Anzeige der verbliebenen Öffnungszeit und Hinweise auf Wartungen.
- Wochenansichten mit Kalenderwoche; Datenstand mit Datum, Uhrzeit und Zeitzone.
- Wochen und Vorgemerkt: einklappbare Tage mit Eventanzahl und Vormerkungszähler; aufgeklappte Tage mit zusätzlichem Abstand. Heute zeigt die Termine direkt.
- Einstellungen > Tage beim Öffnen: Wochenansichten und Vorgemerkt alle aufgeklappt (Standard) oder eingeklappt.
- Sterne speichern konkrete Termine lokal. Eigener Vorgemerkt-Tab für markierte Termine der geladenen Wochen.
- Vormerkungen werden eine Stunde nach bekannter Schließzeit automatisch entfernt, auch nach einem Neustart. Ohne Endzeit wird keine Frist geraten.
- Vorgemerkt ist grün beschriftet, solange ein markiertes RP-Event läuft. Leere eingeklappte Tage sind dezenter dargestellt.
- Drei gespeicherte Teleport-Modi: Kommando kopieren (Standard), direkte Bezirksreise nach zwei Klicks mit 5-Sekunden-Bestätigung oder nach einem Klick.
- Teleporthilfe optional: benötigt Lifestream **2.5.4.4**. Ohne installiertes Lifestream bleiben dessen Buttons verborgen. Direkte Reisen benötigen eine geladene Lifestream-Instanz; keine Lifestream-Dateien werden mitgeliefert.
- Gebaut für Dalamud **API 15**, .NET 10 / Windows x64.

Die Reisehilfe verwendet das in Lifestream 2.5.4.4 statisch untersuchte Grundstück-0-Verhalten und endet am Wohnbezirk, nicht am Haus oder gezielt in der Erweiterung. Dieses Verhalten ist undokumentiert und versionsabhängig. Die Anreise und mögliche Bewegung organisiert Lifestream. Kopieren ist der Standard; direkte Reisen erfolgen erst nach entsprechender Einstellung und bewussten Klicks.

Dies ist ein benutzerdefiniertes Repository, keine Aufnahme in das offizielle Dalamud-Pluginverzeichnis. Ein öffentliches GitHub-Repository und seine Downloads sind für jeden abrufbar; die Beschränkung auf einen Testkreis ist organisatorisch, keine technische Zugriffssperre.

## Test-Rückmeldungen

Bitte Plugin-/Dalamud-/Lifestream-Version, betroffenen Termin, erwartetes und tatsächliches Verhalten sowie bei Bedarf einen zugeschnittenen Screenshot angeben. Keine Zugangsdaten oder vollständigen privaten Logs veröffentlichen.

## Kalenderquelle

[FF14-Light Wiki](https://ff14-light.fandom.com/de/wiki/Kategorie:Eventkalender), Inhalte nach [Fandom-Lizenzhinweisen](https://www.fandom.com/de/licensing-de) / CC BY-SA. Öffentlicher API-Abruf ohne Wiki-Login. Eventseiten werden erst nach Klick im normalen Browser geöffnet. Dies ist keine offizielle Anwendung von Square Enix oder den Wiki-Betreibern.

## Laden und Aktualisieren

Beim Öffnen werden gespeicherte Termine sofort angezeigt. Eine gebündelte Hintergrundprüfung vergleicht Wiki-Revisionen und Versionszeitstempel. Nur geänderte Tagesseiten werden geladen; unveränderte Cachedateien bleiben bestehen. Wiederholte automatische Prüfungen sind auf einmal pro Minute beim Öffnen begrenzt. Neu laden erzwingt einen vollständigen Inhaltsabruf. Beim ersten Start nach dem Update werden ältere Cachedateien einmalig ergänzt. Fehler erhalten die zuletzt gespeicherten Daten mit Warnung.
