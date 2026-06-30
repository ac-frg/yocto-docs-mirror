Defines the kernel type to be used in assembling the configuration.
The linux-yocto recipes define "standard", "tiny", and "preempt-rt"
kernel types. See the ":ref:`kernel-dev/advanced:kernel types`"
section in the
Yocto Project Linux Kernel Development Manual for more information on
kernel types.

You define the :term:`KTYPE` variable in the
:ref:`kernel-dev/advanced:bsp descriptions`. The
value you use must match the value used for the
:term:`LINUX_KERNEL_TYPE` value used by the
kernel recipe.
