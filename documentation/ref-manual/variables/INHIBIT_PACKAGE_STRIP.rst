If set to "1", causes the build to not strip binaries in resulting
packages and prevents the ``-dbg`` package from containing the source
files.

By default, the OpenEmbedded build system strips binaries and puts
the debugging symbols into ``${``\ :term:`PN`\ ``}-dbg``.
Consequently, you should not set :term:`INHIBIT_PACKAGE_STRIP` when you
plan to debug in general.
