After the kernel has been built, this task checks the size of the
stripped kernel image against
:term:`KERNEL_IMAGE_MAXSIZE`. If that
variable was set and the size of the stripped kernel exceeds that size,
the kernel build produces a warning to that effect.
