When using the :ref:`ref-classes-barebox` class, this variable allows you
to specify the name of the barebox defconfig to build.
The name must be a defconfig file known to the barebox build environment.
This variable is mainly useful for generic use cases where a dedicated
configuration is not required.
The :ref:`ref-classes-barebox` class itself already sets it for some QEMU
machines::

   BAREBOX_CONFIG:qemuarm = "multi_v7_defconfig"
   BAREBOX_CONFIG:qemuarm64 = "multi_v8_defconfig"
   BAREBOX_CONFIG:qemux86-64 = "efi_defconfig"

Except for these, the default value of :term:`BAREBOX_CONFIG` is empty.
For more information on how to provide a barebox configuration, see the
:ref:`ref-classes-barebox` class.
