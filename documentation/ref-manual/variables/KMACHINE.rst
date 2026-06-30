The machine as known by the kernel. Sometimes the machine name used
by the kernel does not match the machine name used by the
OpenEmbedded build system. For example, the machine name that the
OpenEmbedded build system understands as ``core2-32-intel-common``
goes by a different name in the Linux Yocto kernel. The kernel
understands that machine as ``intel-core2-32``. For cases like these,
the :term:`KMACHINE` variable maps the kernel machine name to the
OpenEmbedded build system machine name.

These mappings between different names occur in the Yocto Linux
Kernel's ``meta`` branch. As an example take a look in the
``common/recipes-kernel/linux/linux-yocto_3.19.bbappend`` file::

   LINUX_VERSION:core2-32-intel-common = "3.19.0"
   COMPATIBLE_MACHINE:core2-32-intel-common = "${MACHINE}"
   SRCREV_meta:core2-32-intel-common = "8897ef68b30e7426bc1d39895e71fb155d694974"
   SRCREV_machine:core2-32-intel-common = "43b9eced9ba8a57add36af07736344dcc383f711"
   KMACHINE:core2-32-intel-common = "intel-core2-32"
   KBRANCH:core2-32-intel-common = "standard/base"
   KERNEL_FEATURES:append:core2-32-intel-common = " ${KERNEL_FEATURES_INTEL_COMMON}"

The :term:`KMACHINE` statement says
that the kernel understands the machine name as "intel-core2-32".
However, the OpenEmbedded build system understands the machine as
"core2-32-intel-common".
