Specifies the flags to pass to the linker. This variable is exported
to an environment variable and thus made visible to the software
being built during the compilation step.

Default initialization for :term:`LDFLAGS` varies depending on what is
being built:

-  :term:`TARGET_LDFLAGS` when building for the
   target

-  :term:`BUILD_LDFLAGS` when building for the
   build host (i.e. ``-native``)

-  :term:`BUILDSDK_LDFLAGS` when building for
   an SDK (i.e. ``nativesdk-``)
