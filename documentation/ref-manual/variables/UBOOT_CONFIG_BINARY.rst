This variable cannot be set to a value in a config, it is a placeholder
for configuring the :term:`UBOOT_CONFIG` flow via flags::

   UBOOT_CONFIG_BINARY[foo] = "binary1"
   UBOOT_CONFIG_BINARY[bar] = "binary2"

It specifies the binary to select as the one to deploy in :term:`DEPLOY_DIR_IMAGE`.
The output of a U-Boot build may be more than one binary, for example::

   u-boot.bin
   u-boot-with-spl.bin

Setting the ``binary`` value to ``u-boot-with-spl.bin`` will make this
binary the one deployed in :term:`DEPLOY_DIR_IMAGE`. It is renamed to
include the build configuration name in the process (``foo`` or ``bar`` in
the above example).

This option defaults to :term:`UBOOT_BINARY` if not specified.

For more information on how the :term:`UBOOT_CONFIG_BINARY` variable is
handled, see the :ref:`ref-classes-uboot-config` class.
