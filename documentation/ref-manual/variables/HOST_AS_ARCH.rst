Specifies architecture-specific assembler flags.

Default initialization for :term:`HOST_AS_ARCH` varies depending on what
is being built:

-  :term:`TARGET_AS_ARCH` when building for the
   target

-  :term:`BUILD_AS_ARCH` when building for the build host (i.e.
   ``-native``)

-  :term:`SDK_AS_ARCH` when building for an SDK (i.e. ``nativesdk-``)
