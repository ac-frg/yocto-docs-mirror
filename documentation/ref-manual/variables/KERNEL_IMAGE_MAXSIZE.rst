Specifies the maximum size of the kernel image file in kilobytes. If
:term:`KERNEL_IMAGE_MAXSIZE` is set, the size of the kernel image file is
checked against the set value during the
:term:`do_sizecheck` task. The task fails if
the kernel image file is larger than the setting.

:term:`KERNEL_IMAGE_MAXSIZE` is useful for target devices that have a
limited amount of space in which the kernel image must be stored.

By default, this variable is not set, which means the size of the
kernel image is not checked.
