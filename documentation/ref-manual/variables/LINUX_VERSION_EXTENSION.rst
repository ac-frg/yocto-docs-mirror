A string extension compiled into the version string of the Linux
kernel built with the OpenEmbedded build system. You define this
variable in the kernel recipe. For example, the linux-yocto kernel
recipes all define the variable as follows::

   LINUX_VERSION_EXTENSION ?= "-yocto-${LINUX_KERNEL_TYPE}"

Defining this variable essentially sets the Linux kernel
configuration item ``CONFIG_LOCALVERSION``, which is visible through
the ``uname`` command. Here is an example that shows the extension
assuming it was set as previously shown::

   $ uname -r
   3.7.0-rc8-custom
