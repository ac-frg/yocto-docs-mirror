The architecture of the resulting package or packages.

By default, the value of this variable is set to
:term:`TUNE_PKGARCH` when building for the
target, :term:`BUILD_ARCH` when building for the
build host, and "${SDK_ARCH}-${SDKPKGSUFFIX}" when building for the
SDK.

.. note::

   See :term:`SDK_ARCH` for more information.

However, if your recipe's output packages are built specific to the
target machine rather than generally for the architecture of the
machine, you should set :term:`PACKAGE_ARCH` to the value of
:term:`MACHINE_ARCH` in the recipe as follows::

   PACKAGE_ARCH = "${MACHINE_ARCH}"
