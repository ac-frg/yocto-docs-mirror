If :term:`QB_NETWORK_DEVICE` adds more than one network interface to QEMU,
usually the ``ip=`` Linux kernel command line argument needs to be changed
accordingly. The :term:`QB_CMDLINE_IP_SLIRP` variable allows controlling
this value. See the Linux kernel documentation for more details:
https://www.kernel.org/doc/Documentation/filesystems/nfs/nfsroot.txt.
