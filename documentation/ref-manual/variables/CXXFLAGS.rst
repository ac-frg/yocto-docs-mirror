Specifies the flags to pass to the C++ compiler. This variable is
exported to an environment variable and thus made visible to the
software being built during the compilation step.

Default initialization for :term:`CXXFLAGS` varies depending on what is
being built:

-  :term:`TARGET_CXXFLAGS` when building for
   the target

-  :term:`BUILD_CXXFLAGS` when building for the
   build host (i.e. ``-native``)

-  :term:`BUILDSDK_CXXFLAGS` when building
   for an SDK (i.e. ``nativesdk-``)
