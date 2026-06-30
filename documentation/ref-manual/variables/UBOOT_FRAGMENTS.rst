The :term:`UBOOT_FRAGMENTS` variable can be used to pass extra config
fragments from the source tree to ``make`` when U-Boot is configured.
These fragments are located in same ``${S}/configs/`` directory as the
defconfig.

For example::

    UBOOT_MACHINE = "am62x_evm_r5_defconfig"
    UBOOT_FRAGMENTS = "am62x_r5_usbdfu.config"

See the :ref:`ref-classes-uboot-config` class for more information.
