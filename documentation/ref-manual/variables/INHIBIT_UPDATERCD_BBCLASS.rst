Prevents the :ref:`ref-classes-update-rc.d` class from automatically
installing and registering SysV init scripts for packages.

When a recipe inherits the :ref:`ref-classes-update-rc.d` class, init
scripts are typically installed and registered for the packages listed in
:term:`INITSCRIPT_PACKAGES`. This ensures that the relevant
services are started and stopped at the appropriate runlevels using the
traditional SysV init system.

To prevent the build system from adding these scripts and configurations
automatically, set the :term:`INHIBIT_UPDATERCD_BBCLASS` variable as follows::

   INHIBIT_UPDATERCD_BBCLASS = "1"

By default, the value of :term:`INHIBIT_UPDATERCD_BBCLASS` is empty. Setting
it to "0" does not disable inhibition. Only the empty string will disable
inhibition.
