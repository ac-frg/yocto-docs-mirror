Specifies the flags to pass to the C compiler. This variable is
exported to an environment variable and thus made visible to the
software being built during the compilation step.

Default initialization for :term:`CFLAGS` varies depending on what is
being built:

-  :term:`TARGET_CFLAGS` when building for the
   target

-  :term:`BUILD_CFLAGS` when building for the
   build host (i.e. ``-native``)

-  :term:`BUILDSDK_CFLAGS` when building for
   an SDK (i.e. ``nativesdk-``)
