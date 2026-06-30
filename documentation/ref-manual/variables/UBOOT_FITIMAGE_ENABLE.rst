This variable allows to generate a FIT image for U-Boot, which is one
of the ways to implement a verified boot process.

Its default value is "0", so set it to "1" to enable this functionality::

   UBOOT_FITIMAGE_ENABLE = "1"

See the :ref:`ref-classes-uboot-sign` class for details.
