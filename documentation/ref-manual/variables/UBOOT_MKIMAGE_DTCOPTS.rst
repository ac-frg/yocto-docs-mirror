Options for the device tree compiler passed to ``mkimage -D`` feature
while creating a FIT image with the :ref:`ref-classes-kernel-fit-image`
class. If :term:`UBOOT_MKIMAGE_DTCOPTS` is not set then the
:ref:`ref-classes-kernel-fit-image` class will not pass the ``-D`` option
to ``mkimage``.

This variable is also used by the :ref:`ref-classes-uboot-sign` class.
