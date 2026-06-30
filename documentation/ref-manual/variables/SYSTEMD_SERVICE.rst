When inheriting the :ref:`ref-classes-systemd` class,
this variable specifies the systemd service name for a package.

Multiple services can be specified, each one separated by a space.

When you specify this file in your recipe, use a package name
override to indicate the package to which the value applies. Here is
an example from the connman recipe::

   SYSTEMD_SERVICE:${PN} = "connman.service"

The package overrides that can be specified are directly related to the value of
:term:`SYSTEMD_PACKAGES`. Overrides not included in :term:`SYSTEMD_PACKAGES`
will be silently ignored.
