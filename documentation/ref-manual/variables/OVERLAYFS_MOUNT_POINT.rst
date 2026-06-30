When inheriting the :ref:`ref-classes-overlayfs` class,
specifies mount point(s) to be used. For example::

   OVERLAYFS_MOUNT_POINT[data] = "/data"

The assumes you have a ``data.mount`` systemd unit defined elsewhere in
your BSP (e.g. in ``systemd-machine-units`` recipe) and it is installed
into the image. For more information see :ref:`ref-classes-overlayfs`.

.. note::

   Although the :ref:`ref-classes-overlayfs` class is
   inherited by individual recipes, :term:`OVERLAYFS_MOUNT_POINT`
   should be set in your machine configuration.
