Specifies the architecture-specific utility to display information about
ELF files for the build host, and its default definition is derived in
part from :term:`BUILD_PREFIX`::

   BUILD_READELF = "${BUILD_PREFIX}readelf"

When building a :ref:`ref-classes-native` recipe, :term:`READELF` is set
to the value of this variable by default.

The :term:`BUILD_READELF` variable should not be set manually, and is
rarely used in recipes as :term:`READELF` contains the appropriate value
depending on the context (native or target recipes). Exception be made for
target recipes that need to use the utility from the build host at some
point during the build.
