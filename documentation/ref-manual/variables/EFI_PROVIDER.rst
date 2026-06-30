When building bootable images (i.e. where ``hddimg``, ``iso``, or
``wic.vmdk`` is in :term:`IMAGE_FSTYPES`), the
:term:`EFI_PROVIDER` variable specifies the EFI bootloader to use. The
default is "grub-efi", but "systemd-boot" can be used instead.

See the :ref:`ref-classes-systemd-boot` and :ref:`ref-classes-image-live`
classes for more information.
