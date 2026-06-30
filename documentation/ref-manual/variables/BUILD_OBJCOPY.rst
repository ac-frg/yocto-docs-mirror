Specifies the architecture-specific utility to copy object files for the
build host, and its default definition is derived in part from
:term:`BUILD_PREFIX`::

   BUILD_OBJCOPY = "${BUILD_PREFIX}objcopy"

When building a :ref:`ref-classes-native` recipe, :term:`OBJCOPY` is set
to the value of this variable by default.

The :term:`BUILD_OBJCOPY` variable should not be set manually, and is
rarely used in recipes as :term:`OBJCOPY` contains the appropriate value
depending on the context (native or target recipes). Exception be made for
target recipes that need to use the utility from the build host at some
point during the build.
