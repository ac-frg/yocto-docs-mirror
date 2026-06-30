The base name for SDK output files. The default value (as set in
``meta-poky/conf/distro/poky.conf``) is derived from the
:term:`DISTRO`,
:term:`TCLIBC`,
:term:`SDKMACHINE`,
:term:`IMAGE_BASENAME`,
:term:`TUNE_PKGARCH`, and
:term:`MACHINE` variables::

   SDK_NAME = "${DISTRO}-${TCLIBC}-${SDKMACHINE}-${IMAGE_BASENAME}-${TUNE_PKGARCH}-${MACHINE}"
