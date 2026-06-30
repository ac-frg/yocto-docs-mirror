When used with the :ref:`ref-classes-archiver` class,
determines the type of information used to create a released archive.
You can use this variable to create archives of patched source,
original source, configured source, and so forth by employing the
following variable flags (varflags)::

   ARCHIVER_MODE[src] = "original"                   # Uses original (unpacked) source files.
   ARCHIVER_MODE[src] = "patched"                    # Uses patched source files. This is the default.
   ARCHIVER_MODE[src] = "configured"                 # Uses configured source files.
   ARCHIVER_MODE[diff] = "1"                         # Uses patches between do_unpack and do_patch.
   ARCHIVER_MODE[diff-exclude] ?= "file file ..."    # Lists files and directories to exclude from diff.
   ARCHIVER_MODE[dumpdata] = "1"                     # Uses environment data.
   ARCHIVER_MODE[recipe] = "1"                       # Uses recipe and include files.
   ARCHIVER_MODE[srpm] = "1"                         # Uses RPM package files.

For information on how the variable works, see the
``meta/classes/archiver.bbclass`` file in :term:`OpenEmbedded-Core
(OE-Core)`.
