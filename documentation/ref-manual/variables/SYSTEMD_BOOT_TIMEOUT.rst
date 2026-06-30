When :term:`EFI_PROVIDER` is set to
"systemd-boot", the :term:`SYSTEMD_BOOT_TIMEOUT` variable specifies the
boot menu timeout in seconds. By default, the
:ref:`ref-classes-systemd-boot` class sets the
:term:`SYSTEMD_BOOT_TIMEOUT` as follows::

   SYSTEMD_BOOT_TIMEOUT ?= "10"

For information on Systemd-boot, see the `Systemd-boot
documentation <https://www.freedesktop.org/wiki/Software/systemd/systemd-boot/>`__.
