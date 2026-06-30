Configures one or more U-Boot configurations to build. Each
configuration must define the :term:`UBOOT_MACHINE` variable.
Additional control variables are: :term:`UBOOT_CONFIG_BINARY`,
:term:`UBOOT_CONFIG_FRAGMENTS`, :term:`UBOOT_CONFIG_IMAGE_FSTYPES`, and
:term:`UBOOT_CONFIG_MAKE_OPTS`. 

Here is an updated example from the ``meta-freescale`` layer. ::

   UBOOT_CONFIG ??= "sdcard-ifc-secure-boot sdcard-ifc sdcard-qspi lpuart qspi secure-boot nor"

   UBOOT_CONFIG[nor] = "ls1021atwr_nor_defconfig"
   UBOOT_CONFIG[sdcard-ifc] = "ls1021atwr_sdcard_ifc_defconfig"
   UBOOT_CONFIG[sdcard-qspi] = "ls1021atwr_sdcard_qspi_defconfig"
   UBOOT_CONFIG[lpuart] = "ls1021atwr_nor_lpuart_defconfig"
   UBOOT_CONFIG[qspi] = "ls1021atwr_qspi_defconfig"
   UBOOT_CONFIG[secure-boot] = "ls1021atwr_nor_SECURE_BOOT_defconfig"
   UBOOT_CONFIG[sdcard-ifc-secure-boot] = "ls1021atwr_sdcard_ifc_SECURE_BOOT_defconfig"

   UBOOT_CONFIG_BINARY[sdcard-ifc] = "u-boot-with-spl-pbl.bin"
   UBOOT_CONFIG_BINARY[sdcard-qspi] = "u-boot-with-spl-pbl.bin"
   UBOOT_CONFIG_BINARY[sdcard-ifc-secure-boot] = "u-boot-with-spl-pbl.bin"

In this example, all possible seven configurations are selected. Each
configuration specifies "..._defconfig" as :term:`UBOOT_MACHINE`, and
the "sd..." configurations define an individual name for
:term:`UBOOT_CONFIG_BINARY`.

For more information on how the :term:`UBOOT_CONFIG` variable is handled, see the
:ref:`ref-classes-uboot-config` class.
