Specifies the architecture-specific utility to list symbols from object
files for the build host, and its default definition is derived in part
from :term:`BUILD_PREFIX`::

   BUILD_NM = "${BUILD_PREFIX}nm"

When building a :ref:`ref-classes-native` recipe, :term:`NM` is set to the
value of this variable by default.

The :term:`BUILD_NM` variable should not be set manually, and is rarely
used in recipes as :term:`NM` contains the appropriate value depending on
the context (native or target recipes). Exception be made for target
recipes that need to use the utility from the build host at some point
during the build.
