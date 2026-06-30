The :term:`QB_KERNEL_CMDLINE_APPEND` variable controls the options passed
to the Linux kernel's ``-append`` QEMU options, which controls the Linux kernel
command-line.

For example::

   QB_KERNEL_CMDLINE_APPEND = "console=ttyS0"
