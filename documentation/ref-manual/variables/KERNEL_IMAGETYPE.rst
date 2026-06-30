The type of kernel to build for a device, usually set by the machine
configuration files and defaults to "zImage". This variable is used
when building the kernel and is passed to ``make`` as the target to
build.

To build additional kernel image types, use :term:`KERNEL_IMAGETYPES`.
