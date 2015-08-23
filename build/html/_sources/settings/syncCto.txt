Einstellungen SyncCto
=====================

Vorwort
-------
Die Einstellungen von SyncCto sind im Menü unter dem Punkt "Synchronisation/Konfiguration" zu finden.

Hier können diverse Blacklisten/Whitelisten eingestellt werden.

Dateien und Ordner ausschließen
-------------------------------

Ordner:
    Alle Ordner die in dieser Liste stehen, werden nicht geprüft, dementsprechend werden die Daten auch nicht übertragen.

    Es ist möglich Pfade direkt vom Root anzugeben "system/html" oder mit Wildcards zu arbeiten. Hierbei gib es allerdings nur die Möglichkeit mit dem \*-Operator zu arbeiten. So können zum Beispiel alle Verzeichnisse die "htlm" im Namen haben, ignoriert werden.

Dateien:
    Genau wie bei den Ordnern, ist es möglich einzelne Dateien auf die Blacklist zu setzten.

    - Alle Dateien mit dem gleichen Name
        Sollte nur eine Dateiname angegeben werden, so werden alle Dateien mit diesem Namen ignoriert.
    - Datei mit einem Bestimmten Pfad
        Wird zusätzlich zum Dateiname noch ein Pfad angegeben, wird nur diese eine Datei ignoriert.
    - Dateien im TL_ROOT
        Sollen Dateien im TL_ROOT ignoriert werden, muss ein "TL_ROOT" hinzugefügt werden.


Erlaubte Ordner im Stammverzeichnis - Erlaubte Ordner
-----------------------------------------------------

In dieser Liste werden alle Ordner angegeben, die synchronisiert werden sollen. Dies ist dafür gut wenn neben der Contao Installation noch andere CMS oder Foren installiert sind, die nicht synchronisiert werden sollen.

Sollte eine Erweiterung wie Isotope installiert sein, müssen die zusätzlichen Ordner die im Root von Contao angelegt wurden, hier hinzugefügt werden. Da sonst die Bilder des Shops nicht mit hochgeladen werden.

localconfig.php Einträge ausschließen
-------------------------------------

In dieser Liste werden alle Einträge ausgegeben die in der Localconfig stehen oder stehen könnten. Hierbei werden die DCA Dateien ausgelesen um alle Einstellungen zu ermitteln. Jede aktivierte Einstellung wird nicht auf den Client übertragen.


Nicht empfohlene Tabellen
-------------------------

Diese Liste enthält alle Datenbanken-Tabellen des Systems. Jede Tabelle die hier aktiviert ist, wird während der Synchronisation als "Nicht empfohlen" angezeigt. Dies bedeutet, dass ein Benutzter einen Hinweis bekommt, dass diese Tabellen empfindliche Inhalte besitzen. Allerdings können Sie noch immer übertragen werden.

Versteckte Tabellen
-------------------

Diese Liste enthält alle Datenbank-Tabellen des Systems. Jede Tabelle die hier aktiviert ist, wird nicht in der Synchronisation angezeigt und auch nicht im Backup Menü. 

Experten-Einstellungen
----------------------

Debugmodus aktivieren:
    Wenn aktiviert, werden zusätzliche Inhalte während der Synchronisation ausgegeben. Zudem wird eine Log-Datei erstellt welche die Kommunikation wiederspiegelt.

Experten-Einstellungen aktivieren:

    - "wait_timeout" konfigurieren
        Diese Wert wird in der Verbindung mit "MySQL Server has gone away" verwendet. Sollte dieser Fehle auftreten lohnt es sich den Wert auf "28000" zu setzten.
    - "interactive_timeout" konfigurieren
        Diese Wert wird in der Verbindung mit "MySQL Server has gone away" verwendet. Sollte dieser Fehle auftreten lohnt es sich den Wert auf "28000" zu setzten.
    - Datenbank Abfragelimit
        Diese Wert wird in der Verbindung mit "MySQL Server has gone away" verwendet. Sollte dieser Fehle auftreten lohnt es sich den Wert auf "500" zu setzten.

Automatische Aktualisierung der Datenbank:

