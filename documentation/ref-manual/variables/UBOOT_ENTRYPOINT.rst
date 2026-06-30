Specifies the entry point for the U-Boot image. During U-Boot image
creation, the :term:`UBOOT_ENTRYPOINT` variable is passed as a
command-line parameter to the ``uboot-mkimage`` utility.

To pass a 64 bit address for FIT image creation, you will need to set:
-  The :term:`FIT_ADDRESS_CELLS` variable for FIT image creation.
-  The :term:`UBOOT_FIT_ADDRESS_CELLS` variable for U-Boot FIT image creation.

This variable is used by the :ref:`ref-classes-kernel-fit-image`,
:ref:`ref-classes-kernel-uimage`, :ref:`ref-classes-kernel`,
:ref:`ref-classes-uboot-config` and :ref:`ref-classes-uboot-sign`
classes.
