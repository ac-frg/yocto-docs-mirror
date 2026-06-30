When using ``runqemu``, the :term:`QB_NFSROOTFS_EXTRA_OPT` variable
controls extra options to be appended to the NFS rootfs options in the
Linux kernel command-line.

For example::

   QB_NFSROOTFS_EXTRA_OPT = "wsize=4096,rsize=4096"
