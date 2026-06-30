When the :ref:`ref-classes-overlayfs-etc` class is
inherited, specifies the file system type for the read/write
layer of ``/etc``. There is no default, so you must set this if you
wish to enable :ref:`ref-classes-overlayfs-etc`,
for example, assuming the file system is ext4::

   OVERLAYFS_ETC_FSTYPE = "ext4"
