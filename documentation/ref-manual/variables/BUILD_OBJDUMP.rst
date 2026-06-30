Specifies the architecture-specific utility to display object files
information for the build host, and its default definition is derived in
part from :term:`BUILD_PREFIX`::

   BUILD_OBJDUMP = "${BUILD_PREFIX}objdump"

When building a :ref:`ref-classes-native` recipe, :term:`OBJDUMP` is set
to the value of this variable by default.

The :term:`BUILD_OBJDUMP` variable should not be set manually, and is
rarely used in recipes as :term:`OBJDUMP` contains the appropriate value
depending on the context (native or target recipes). Exception be made for
target recipes that need to use the utility from the build host at some
point during the build.
