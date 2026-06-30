Specifies the options to pass to ``update-rc.d``. Here is an example::

   INITSCRIPT_PARAMS = "start 99 5 2 . stop 20 0 1 6 ."

In this example, the script has a runlevel of 99, starts the script
in initlevels 2 and 5, and stops the script in levels 0, 1 and 6.

The variable's default value is "defaults", which is set in the
:ref:`ref-classes-update-rc.d` class.

The value in :term:`INITSCRIPT_PARAMS` is passed through to the
``update-rc.d`` command. For more information on valid parameters,
please see the manual page: :manpage:`update-rc.d <update-rc.d(8)>`.
