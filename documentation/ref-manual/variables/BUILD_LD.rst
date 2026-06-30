Specifies the linker command for the build host, and its default
definition is derived in part from :term:`BUILD_PREFIX` and
:term:`BUILD_LD_ARCH`::

   BUILD_LD = "${BUILD_PREFIX}ld ${BUILD_LD_ARCH}"

When building a :ref:`ref-classes-native` recipe, :term:`LD` is set to the
value of this variable by default.

The :term:`BUILD_LD` variable should not be set manually, and is rarely
used in recipes as :term:`LD` contains the appropriate value depending on
the context (native or target recipes). Exception be made for target
recipes that need to use the linker from the build host at some point
during the build.
