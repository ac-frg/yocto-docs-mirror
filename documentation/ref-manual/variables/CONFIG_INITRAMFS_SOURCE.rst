Identifies the initial RAM filesystem (:term:`Initramfs`) source files. The
OpenEmbedded build system receives and uses this kernel Kconfig
variable as an environment variable. By default, the variable is set
to null ("").

The :term:`CONFIG_INITRAMFS_SOURCE` can be either a single cpio archive
with a ``.cpio`` suffix or a space-separated list of directories and
files for building the :term:`Initramfs` image. A cpio archive should contain
a filesystem archive to be used as an :term:`Initramfs` image. Directories
should contain a filesystem layout to be included in the :term:`Initramfs`
image. Files should contain entries according to the format described
by the ``usr/gen_init_cpio`` program in the kernel tree.

If you specify multiple directories and files, the :term:`Initramfs` image
will be the aggregate of all of them.

For information on creating an :term:`Initramfs`, see the
":ref:`dev-manual/building:building an initial ram filesystem (Initramfs) image`" section
in the Yocto Project Development Tasks Manual.
