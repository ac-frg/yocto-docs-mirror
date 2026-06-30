This variable allows to add a U-Boot script as a text file to the
FIT image. Such a script can be sourced from the U-Boot shell.

When inheriting the :ref:`ref-classes-kernel-fit-image` class a
script file should be included in the :term:`SRC_URI` of the Linux
kernel recipe.

Example:

-  Add a script ``boot.cmd`` to the Linux kernel recipe::

      FIT_UBOOT_ENV = "boot.cmd"
      SRC_URI += "file://${FIT_UBOOT_ENV}"

-  Use the script file from the U-Boot shell. The name of the script in
   FIT image is ``bootscr-${FIT_UBOOT_ENV}``. This example loads the FIT
   image from a TFTP server::

      tftp $loadaddr $fit_tftp_path
      source $loadaddr#bootscr-boot.cmd

More information can be found in the official U-Boot documentation:
`U-Boot source command <https://docs.u-boot.org/en/latest/usage/cmd/source.html#fit-image.f>`__
