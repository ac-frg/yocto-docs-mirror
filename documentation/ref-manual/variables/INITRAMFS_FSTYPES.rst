Defines the format for the output image of an initial RAM filesystem
(:term:`Initramfs`), which is used during boot. Supported formats are the
same as those supported by the
:term:`IMAGE_FSTYPES` variable.

The default value of this variable, which is set in the
``meta/conf/bitbake.conf`` configuration file in
:term:`OpenEmbedded-Core (OE-Core)`, is "cpio.gz". The Linux kernel's
:term:`Initramfs` mechanism, as opposed to the initial RAM filesystem
:wikipedia:`initrd <Initrd>` mechanism, expects
an optionally compressed cpio archive.
