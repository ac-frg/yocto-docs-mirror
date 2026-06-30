If redundant environment support is enabled in U-boot's configuration,
this variable should be set to properly generate the redundant environment
in the output U-boot environment binary file.

Its default value is "0", set it to "1" to enable this functionality::

   UBOOT_INITIAL_ENV_BINARY_REDUND = "1"

The :term:`UBOOT_INITIAL_ENV_BINARY` must also be set to "1" if
:term:`UBOOT_INITIAL_ENV_BINARY_REDUND` is enabled.

This variable is used in the :ref:`ref-classes-uboot-config` class.
