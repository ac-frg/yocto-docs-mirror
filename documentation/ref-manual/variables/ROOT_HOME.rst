Defines the root home directory. By default, this directory is set as
follows in the BitBake configuration file::

   ROOT_HOME ??= "/home/root"

.. note::

   This default value is likely used because some embedded solutions
   prefer to have a read-only root filesystem and prefer to keep
   writeable data in one place.

When setting ``INIT_MANAGER = systemd``, the default will be set to::

   ROOT_HOME ?= "/root"

You can also override the default by setting the variable in your distro
configuration or in the ``local.conf`` file.
