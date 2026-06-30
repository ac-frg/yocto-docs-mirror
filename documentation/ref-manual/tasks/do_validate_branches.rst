After the kernel is unpacked but before it is patched, this task makes
sure that the machine and metadata branches as specified by the
:term:`SRCREV` variables actually exist on the specified
branches. Otherwise, if :term:`AUTOREV` is not being used, the
:term:`do_validate_branches` task fails during the build.
