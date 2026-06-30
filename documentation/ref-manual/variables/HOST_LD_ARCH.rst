Specifies architecture-specific linker flags.

Default initialization for :term:`HOST_LD_ARCH` varies depending on what
is being built:

-  :term:`TARGET_LD_ARCH` when building for the target

-  :term:`BUILD_LD_ARCH` when building for the build host (i.e.
   ``-native``)

-  :term:`SDK_LD_ARCH` when building for an SDK (i.e. ``nativesdk-``)
