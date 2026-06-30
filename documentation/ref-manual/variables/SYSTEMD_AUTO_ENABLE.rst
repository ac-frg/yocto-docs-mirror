When inheriting the :ref:`ref-classes-systemd` class,
this variable specifies whether the specified service in
:term:`SYSTEMD_SERVICE` should start
automatically or not. By default, the service is enabled to
automatically start at boot time. The default setting is in the
:ref:`ref-classes-systemd` class as follows::

   SYSTEMD_AUTO_ENABLE ??= "enable"

You can disable the service by setting the variable to "disable".
