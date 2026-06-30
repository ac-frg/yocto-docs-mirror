.. warning::

   This variable is deprecated in favor of the ``--sector-size`` wic
   command-line argument. See :ref:`ref-migration-6-0-wic-sector-size-change`
   for more information.

The variable :term:`WIC_SECTOR_SIZE` controls the sector size of Wic
images. In the background, this controls the value of the
``PARTED_SECTOR_SIZE`` environment variable passed to the ``parted``
command-line utility, used to generated the images. The default value is
``512``.

For more information on how to create Wic images, see the
":ref:`dev-manual/wic:creating partitioned images using wic`" section in
the Yocto Project Development Tasks Manual.
