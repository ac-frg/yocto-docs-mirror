Specifies the value of the ``#address-cells`` value for the
description of the FIT image.

The default value is set to "1" by the :ref:`ref-classes-kernel-fit-image`
class, which corresponds to 32 bit addresses.

For platforms that need to set 64 bit addresses, for example in
:term:`UBOOT_LOADADDRESS` and :term:`UBOOT_ENTRYPOINT`, you need to
set this value to "2", as two 32 bit values (cells) will be needed
to represent such addresses.

Here is an example setting "0x400000000" as a load address::

   FIT_ADDRESS_CELLS = "2"
   UBOOT_LOADADDRESS = "0x04 0x00000000"

See `more details about #address-cells <https://elinux.org/Device_Tree_Usage#How_Addressing_Works>`__.
