Hooks
=====

syncExecuteFinalOperations
--------------------------
Call user functions like update db, remove files or anything else.
Called after main synchronisation (db, files, maintenance).
Called directly on the client.

.. code-block:: php

    // config.php
    $GLOBALS['TL_HOOKS']['syncExecuteFinalOperations'][] = array('MyClass', 'MyFunction');

    // Class file.
    class MyClass extends \Backend
    {
        public function MyFunction()
        {
                // Do something
        }
    }

syncDBUpdate
------------
Execute SQL-Commands after DB synchronisation.
Only for SyncTo. SQL is create on Server and send to the client.

.. code-block:: php

    // config.php
    $GLOBALS['TL_HOOKS']['syncDBUpdate'][] = array('MyClass', 'MyFunction');

     // Class file.
    class MyClass extends \Backend
    {
        public function MyFunction($intClientID, $arrSQL)
        {
            // Do something

            // Merge last sql with new ones
            return array_merge((array) $arrSQL, array(
                        array(
                            'prepare' => 'DELETE FOMR tl_content WHERE id=?',
                            'execute' => 1,
                        ),
                    ));
        }
    }

syncDBUpdateBeforeDrop
----------------------
Execute query command before the old tables are dropped.
Temp tables get the prefix "synccto_temp\_".
Only for SyncTo. SQL is create on Server and send to the client.

.. code-block:: php

    // config.php
    $GLOBALS['TL_HOOKS']['syncDBUpdateBeforeDrop'][] = array('MyClass', 'MyFunction');

     // Class file.
    class MyClass extends \Backend
    {
        public function MyFunction($intClientID, $arrSyncTables, $arrLastSQL)
        {
            // Do something

            // Merge last sql with new ones
            return array_merge( (array) $arrLastSQL ,array(
                array(
                    'query' => 'DELETE ...'
                ),
                array(
                    'query' => 'INSERT INTO ...'
                ),
                array(
                    'query' => 'UPDATE ...'
                ),
            ));
        }
    }

syncAdditionalMaintenance
-------------------------
Called after the maintenance from syncCto.

.. code-block:: php

    // config.php
    $GLOBALS['TL_HOOKS']['syncAdditionalMaintenance'][] = array('MyClass', 'MyFunction');

     // Class file.
    class MyClass extends \Backend
    {
        public function MyFunction($arrSetings)
        {
                // To something
        }
    }
