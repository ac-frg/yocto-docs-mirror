This variable allows to add additional environment variables or a script
to be installed together with U-Boot.
This file, typically ``uEnv.txt`` or ``boot.cmd``, is installed in
``/boot`` as well as copied to the :term:`DEPLOYDIR` directory.

For machine configurations needing one of these files a ``.bbappend``
file should include it in the :term:`SRC_URI` of the U-Boot recipe.

If the variable :term:`UBOOT_ENV_SUFFIX` is set to ``scr`` the script is
packaged as a uImage (``mkimage -T script..``) otherwise it gets
installed verbatim.

Some examples:

-  Adding a script ``boot.cmd`` as a uImage to ``/boot``::

      UBOOT_ENV = "boot"
      UBOOT_ENV_SUFFIX = "scr"
      SRC_URI += "file://${UBOOT_ENV_SRC}"

-  Adding a script ``uEnv.txt`` as a plain text file to ``/boot``::

      UBOOT_ENV = "uEnv"
      UBOOT_ENV_SUFFIX = "txt"
      SRC_URI += "file://${UBOOT_ENV_BINARY}"
