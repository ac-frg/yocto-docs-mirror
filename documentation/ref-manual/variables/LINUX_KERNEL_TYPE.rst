Defines the kernel type to be used in assembling the configuration.
The linux-yocto recipes define "standard", "tiny", and "preempt-rt"
kernel types. See the ":ref:`kernel-dev/advanced:kernel types`"
section in the
Yocto Project Linux Kernel Development Manual for more information on
kernel types.

If you do not specify a :term:`LINUX_KERNEL_TYPE`, it defaults to
"standard". Together with :term:`KMACHINE`, the
:term:`LINUX_KERNEL_TYPE` variable defines the search arguments used by
the kernel tools to find the appropriate description within the
kernel :term:`Metadata` with which to build out the sources
and configuration.
