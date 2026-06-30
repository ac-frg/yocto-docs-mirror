When the :ref:`ref-classes-overlayfs-etc` class is
inherited, specifies the device to be mounted for the read/write
layer of ``/etc``. There is no default, so you must set this if you
wish to enable :ref:`ref-classes-overlayfs-etc`, for
example, assuming ``/dev/mmcblk0p2`` was the desired device::

   OVERLAYFS_ETC_DEVICE = "/dev/mmcblk0p2"
