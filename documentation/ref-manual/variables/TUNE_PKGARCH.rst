The package architecture understood by the packaging system to define
the architecture, ABI, and tuning of output packages. The specific
tune is defined using the "_tune" override as follows::

   TUNE_PKGARCH:tune-tune = "tune"

These tune-specific package architectures are defined in the machine
include files. Here is an example of the "core2-32" tuning as used in
the ``meta/conf/machine/include/x86/tune-core2.inc`` file::

   TUNE_PKGARCH:tune-core2-32 = "core2-32"
