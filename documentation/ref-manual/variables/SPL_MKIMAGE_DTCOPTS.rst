Options for the device tree compiler passed to ``mkimage -D`` feature
while creating a FIT image with the :ref:`ref-classes-uboot-sign`
class. If :term:`SPL_MKIMAGE_DTCOPTS` is not set then the
:ref:`ref-classes-uboot-sign` class will not pass the ``-D`` option
to ``mkimage``.

The default value is set to "" by the :ref:`ref-classes-uboot-config`
class.
