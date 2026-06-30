Specifies the architecture-specific utility to generate indexes for
archives for the build host, and its default definition is derived in part
from :term:`BUILD_PREFIX`::

   BUILD_RANLIB = "${BUILD_PREFIX}ranlib -D"

When building a :ref:`ref-classes-native` recipe, :term:`RANLIB` is set to
the value of this variable by default.

The :term:`BUILD_RANLIB` variable should not be set manually, and is
rarely used in recipes as :term:`RANLIB` contains the appropriate value
depending on the context (native or target recipes). Exception be made for
target recipes that need to use the utility from the build host at some
point during the build.
