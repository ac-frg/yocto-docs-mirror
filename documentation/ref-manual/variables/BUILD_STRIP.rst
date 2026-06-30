Specifies the command to be used to strip debugging symbols from binaries
produced for the build host, and its default definition is derived in part
from :term:`BUILD_PREFIX`::

   BUILD_STRIP = "${BUILD_PREFIX}strip"

When building a :ref:`ref-classes-native` recipe, :term:`STRIP` is set to
the value of this variable by default.

The :term:`BUILD_STRIP` variable should not be set manually, and is
rarely used in recipes as :term:`STRIP` contains the appropriate value
depending on the context (native or target recipes). Exception be made for
target recipes that need to use the utility from the build host at some
point during the build.
