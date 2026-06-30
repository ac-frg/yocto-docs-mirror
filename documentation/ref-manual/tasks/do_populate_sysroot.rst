Stages (copies) a subset of the files installed by the
:term:`do_install` task into the appropriate
sysroot. For information on how to access these files from other
recipes, see the :term:`STAGING_DIR* <STAGING_DIR_HOST>` variables.
Directories that would typically not be needed by other recipes at build
time (e.g. ``/etc``) are not copied by default.

For information on what directories are copied by default, see the
:term:`SYSROOT_DIRS* <SYSROOT_DIRS>` variables. You can change
these variables inside your recipe if you need to make additional (or
fewer) directories available to other recipes at build time.

The :term:`do_populate_sysroot` task is a shared state (sstate) task, which
means that the task can be accelerated through sstate use. Realize also
that if the task is re-executed, any previous output is removed (i.e.
"cleaned").
