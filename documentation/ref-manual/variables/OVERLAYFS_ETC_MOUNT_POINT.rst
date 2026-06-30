When the :ref:`ref-classes-overlayfs-etc` class is
inherited, specifies the parent mount path for the filesystem layers.
There is no default, so you must set this if you wish to enable
:ref:`ref-classes-overlayfs-etc`, for example if the desired path is
"/data"::

   OVERLAYFS_ETC_MOUNT_POINT = "/data"
