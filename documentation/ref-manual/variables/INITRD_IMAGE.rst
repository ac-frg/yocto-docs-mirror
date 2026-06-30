When building a "live" bootable image (i.e. when
:term:`IMAGE_FSTYPES` contains "live"),
:term:`INITRD_IMAGE` specifies the image recipe that should be built to
provide the initial RAM disk image. The default value is
"core-image-minimal-initramfs".

See the :ref:`ref-classes-image-live` class for more information.
