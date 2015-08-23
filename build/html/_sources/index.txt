.. raw:: html

    <style>
        .header {
            display: block;
            width:100%;
        }

        .header .text {
            display: inline;
            float: left;
        }

        .header .img {
            display: inline;
            float: right;
        }

        .clearfix:after {
            content: ".";
            clear: both;
            display: block;
            visibility: hidden;
            height: 0px;
        }
    </style>

    <div class="header clearfix">
        <div class="text">
            <h1>SyncCto - Handbuch</h1>
        </div>
        <div class="img">
            <img src="_static/logo.png" alt="SyncCto Handbuch" />
        </div>
    </div>


Was ist SyncCto?
----------------

SyncCto bietet die Möglichkeit mehrere Contao-Installationen auf Basis einer Grund-Installation zu synchronisieren.

Alle Aktionen können bequem im Backend durchgeführt werden. Durch die Integration in das Contao Rechtesystem können auch Redakteure eine Auswahl vorher definierter Datenbank-Tabellen und Dateien synchronisieren.

Ein integrierter Backup-Manager sichert ausgewählte Datenbank-Tabellen, wahlweise die gesamte Contao-Installation oder nur die persönlichen Daten. Angelegte Backups können durch den Backup-Manager auch wieder importiert werden.

Durch die Verwendung von syncCto können Redakteure schnell und einfach in einem Preview-System arbeiten und bei Vollendung der Arbeit den aktuellen und freigegebenen Stand zum Live-System synchronisieren.

Einstellungen
-------------

.. toctree::
    :glob:
    :maxdepth: 2

    settings/*

Workflow
--------

.. toctree::
    :glob:
    :maxdepth: 2

    workflow/*

Hook
----

.. toctree::
    :glob:
    :maxdepth: 2

    hooks/*

Sonstiges
---------

.. toctree::
    :glob:
    :maxdepth: 2

    miscellaneous/*

Indices and tables
==================

* :ref:`genindex`
