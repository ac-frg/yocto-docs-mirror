Specifies architecture-specific compiler flags that are passed to the
C compiler.

Default initialization for :term:`HOST_CC_ARCH` varies depending on what
is being built:

-  :term:`TARGET_CC_ARCH` when building for the
   target

-  :term:`BUILD_CC_ARCH` when building for the build host (i.e.
   ``-native``)

-  :term:`SDK_CC_ARCH` when building for an SDK (i.e. ``nativesdk-``)
