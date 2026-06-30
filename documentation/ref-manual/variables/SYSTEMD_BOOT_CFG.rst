When :term:`EFI_PROVIDER` is set to
"systemd-boot", the :term:`SYSTEMD_BOOT_CFG` variable specifies the
configuration file that should be used. By default, the
:ref:`ref-classes-systemd-boot` class sets the
:term:`SYSTEMD_BOOT_CFG` as follows::

   SYSTEMD_BOOT_CFG ?= "${S}/loader.conf"

For information on Systemd-boot, see the `Systemd-boot
documentation <https://www.freedesktop.org/wiki/Software/systemd/systemd-boot/>`__.
