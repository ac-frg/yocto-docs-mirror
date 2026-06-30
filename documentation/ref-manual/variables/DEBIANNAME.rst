When the :ref:`ref-classes-debian` class is inherited,
which is the default behavior, :term:`DEBIANNAME` allows you to override
the library name for an individual package. Overriding the library
name in these cases is rare. You must use the package name as an
override when you set this variable. Here is an example from the
``dbus`` recipe::

   DEBIANNAME:${PN} = "dbus-1"
