If ``KERNEL_IMAGE_STRIP_EXTRA_SECTIONS`` is defined, this task strips
the sections named in that variable from ``vmlinux``. This stripping is
typically used to remove nonessential sections such as ``.comment``
sections from a size-sensitive configuration.
