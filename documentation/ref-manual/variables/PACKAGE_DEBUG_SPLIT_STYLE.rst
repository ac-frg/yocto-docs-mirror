Determines how to split up and package debug and source information
when creating debugging packages to be used with the GNU Project
Debugger (GDB). In general, based on the value of this variable,
you can combine the source and debug info in a single package,
you can break out the source into a separate package that can be
installed independently, or you can choose to not have the source
packaged at all.

The possible values of :term:`PACKAGE_DEBUG_SPLIT_STYLE` variable:

-  "``.debug``": All debugging and source info is placed in a single
   ``*-dbg`` package; debug symbol files are placed next to the
   binary in a ``.debug`` directory so that, if a binary is installed
   into ``/bin``, the corresponding debug symbol file is installed
   in ``/bin/.debug``. Source files are installed in the same ``*-dbg``
   package under ``/usr/src/debug``.

-  "``debug-file-directory``": As above, all debugging and source info
   is placed in a single ``*-dbg`` package; debug symbol files are
   placed entirely under the directory ``/usr/lib/debug`` and separated
   by the path from where the binary is installed, so that if a binary
   is installed in ``/bin``, the corresponding debug symbols are installed
   in ``/usr/lib/debug/bin``, and so on. As above, source is installed
   in the same package under ``/usr/src/debug``.

-  "``debug-with-srcpkg``": Debugging info is placed in the standard
   ``*-dbg`` package as with the ``.debug`` value, while source is
   placed in a separate ``*-src`` package, which can be installed
   independently.  This is the default setting for this variable,
   as defined in :term:`OE-Core <OpenEmbedded-Core (OE-Core)>`'s ``bitbake.conf`` file.

-  "``debug-without-src``": The same behavior as with the ``.debug``
   setting, but no source is packaged at all.

.. note::

   Much of the above package splitting can be overridden via
   use of the :term:`INHIBIT_PACKAGE_DEBUG_SPLIT` variable.

You can find out more about debugging using GDB by reading the
":ref:`dev-manual/debugging:debugging with the gnu project debugger (gdb) remotely`" section
in the Yocto Project Development Tasks Manual.
