Includes additional kernel metadata. In the OpenEmbedded build
system, the default Board Support Packages (BSPs)
:term:`Metadata` is provided through the
:term:`KMACHINE` and :term:`KBRANCH`
variables. You can use the :term:`KERNEL_FEATURES` variable from within
the kernel recipe or kernel append file to further add metadata for
all BSPs or specific BSPs.

The metadata you add through this variable includes config fragments
and features descriptions, which usually includes patches as well as
config fragments. You typically override the :term:`KERNEL_FEATURES`
variable for a specific machine. In this way, you can provide
validated, but optional, sets of kernel configurations and features.

For example, the following example from the ``linux-yocto-rt_4.12``
kernel recipe adds "netfilter" and "taskstats" features to all BSPs
as well as "virtio" configurations to all QEMU machines. The last two
statements add specific configurations to targeted machine types::

   KERNEL_EXTRA_FEATURES ?= "features/netfilter/netfilter.scc features/taskstats/taskstats.scc"
   KERNEL_FEATURES:append = " ${KERNEL_EXTRA_FEATURES}"
   KERNEL_FEATURES:append:qemuall = " cfg/virtio.scc"
   KERNEL_FEATURES:append:qemux86 = "  cfg/sound.scc cfg/paravirt_kvm.scc"
   KERNEL_FEATURES:append:qemux86-64 = " cfg/sound.scc"
