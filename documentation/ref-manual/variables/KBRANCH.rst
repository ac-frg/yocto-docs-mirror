A regular expression used by the build process to explicitly identify
the kernel branch that is validated, patched, and configured during a
build. You must set this variable to ensure the exact kernel branch
you want is being used by the build process.

Values for this variable are set in the kernel's recipe file and the
kernel's append file. For example, if you are using the
``linux-yocto_4.12`` kernel, the kernel recipe file is the
``meta/recipes-kernel/linux/linux-yocto_4.12.bb`` file. :term:`KBRANCH`
is set as follows in that kernel recipe file::

   KBRANCH ?= "standard/base"

This variable is also used from the kernel's append file to identify
the kernel branch specific to a particular machine or target
hardware. Continuing with the previous kernel example, the kernel's
append file is located in the
BSP layer for a given machine. For example, the append file for the
Beaglebone and generic versions of both 32 and 64-bit IA
machines (``meta-yocto-bsp``) is named
``meta-yocto-bsp/recipes-kernel/linux/linux-yocto_6.1.bbappend``.
Here are the related statements from that append file::

   KBRANCH:genericx86  = "v6.1/standard/base"
   KBRANCH:genericx86-64  = "v6.1/standard/base"
   KBRANCH:beaglebone-yocto = "v6.1/standard/beaglebone"

The :term:`KBRANCH` statements
identify the kernel branch to use when building for each supported
BSP.
