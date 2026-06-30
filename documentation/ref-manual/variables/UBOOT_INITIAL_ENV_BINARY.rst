This variable enables the generation of the U-Boot initial environment in
binary format.

Its default value is "0", set it to "1" to enable this functionality::

   UBOOT_INITIAL_ENV_BINARY = "1"

If set to "1", you must also set the size of the environment with
:term:`UBOOT_INITIAL_ENV_BINARY_SIZE`.

This variable is used in the :ref:`ref-classes-uboot-config` class.

The resulting binary can be flashed using :doc:`WIC </dev-manual/wic>` or
any other flashing method at the environment offset, overriding any
existing environment if one is present. Below is an example of a WKS file
to flash the binary::

   part --source rawcopy --sourceparams="file=u-boot-initial-env-sd.bin" --ondisk sda --no-table --offset 4096k

In this example, the U-Boot initial environment binary
`u-boot-initial-env-sd.bin` is flashed at offset 4096 kibibyte.
