The Linux version from ``kernel.org`` on which the Linux kernel image
being built using the OpenEmbedded build system is based. You define
this variable in the kernel recipe. For example, the
``linux-yocto-3.4.bb`` kernel recipe found in
``meta/recipes-kernel/linux`` defines the variables as follows::

   LINUX_VERSION ?= "3.4.24"

The :term:`LINUX_VERSION` variable is used to define :term:`PV`
for the recipe::

   PV = "${LINUX_VERSION}+git"
