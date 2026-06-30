The variable :term:`OPKGBUILDCMD` specifies the command used to build opkg
packages when using the :ref:`ref-classes-package_ipk` class. It is
defined in :ref:`ref-classes-package_ipk` as::

    OPKGBUILDCMD ??= 'opkg-build -Z zstd -a "${ZSTD_DEFAULTS}"'
