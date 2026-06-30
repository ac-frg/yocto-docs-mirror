Specifies the flags to pass to the C pre-processor (i.e. to both the
C and the C++ compilers). This variable is exported to an environment
variable and thus made visible to the software being built during the
compilation step.

Default initialization for :term:`CPPFLAGS` varies depending on what is
being built:

-  :term:`TARGET_CPPFLAGS` when building for
   the target

-  :term:`BUILD_CPPFLAGS` when building for the
   build host (i.e. ``-native``)

-  :term:`BUILDSDK_CPPFLAGS` when building
   for an SDK (i.e. ``nativesdk-``)
