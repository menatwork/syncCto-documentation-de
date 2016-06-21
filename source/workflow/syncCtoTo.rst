Workflow SyncCto To
===================

SyncTo bedeutet das alle Daten vom Server auf den Client geladen werden. In der Vorauswahl kann eingestellt werden, was zum Client übertragen werden soll.

Dateien synchronisieren
-----------------------
    - Contao-Installation
        Alle Dateien die für Contao wichtig sind, wie zum Beispiel: assets, composer, contao, share, etc.
        Die Ordner können über die SyncCto Einstellungen angepasst werden. Siehe hierzu "Erlaubte Ordner im Stammverzeichnis - Erlaubte Ordner"

    - Dateiverwaltung (files)
        Hierrunter fallen alle Dateien die sich im Ordner Files befinden. Über die Blacklisten können Ordner oder Dateien ausgeschlossen werden.

    - Veränderte Daten
        Veränderte Daten, ist die Prüfung ob bestehende Dateien sich geändert haben oder neue hinzugekommen sind.

    - Gelöschte Daten
        Gelöscht Daten, ist die Prüfung ob Dateien die nicht mehr auf dem Server vorhanden sind, noch auf dem Client existieren.

    - Konfigurationsdateien
        Hierrunter fallen alle Einstellungen der Local-Config von Contao. Auch diese können über die Einstellungen angepasst werden.


    - Datenbank synchronisieren
        Abgleich der Datenbank. Während der Synchronisation wird eine Übersicht angezeigt, welche Tabellen sich geändert haben.

    - 'tl-files' überschreiben
        Überträgt die Tabelle "tl-files" des DBAF von Contao. Ohne diese Option versucht das System die Daten zu immigrieren.

Systemwartung aktivieren
------------------------

    - Datenbank-Cache
        Leeren aller Contao Caches der Datenbank.

    - Datei-Cache
        Leeren der Datei Caches von Contao.

    - XML-Dateien
        Neu erstellen der XML Daten.

Warnhinweis deaktivieren
------------------------
Deaktiviert die Warnung die beim SyncFrom aktiviert wurde.

Fehlermeldungen anzeigen
------------------------
Aktivieren der Option "Fehlermeldungen anzeigen" von Contao. Wenn aktiviert, zeigt Contao die Fehlermeldungen direkt auf der Webseite an. Ist dieser Option nicht aktiviert wird die Option auch auf dem Client deaktiviert.
Wichtig: Diese Option sollte nicht für Produktiv System benutzt werden.

