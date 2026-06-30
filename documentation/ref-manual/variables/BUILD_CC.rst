Specifies the architecture-specific C compiler for the build host,
and its default definition is derived in part from :term:`BUILD_PREFIX`
and :term:`BUILD_CC_ARCH`::

   BUILD_CC = "${CCACHE}${BUILD_PREFIX}gcc ${BUILD_CC_ARCH}"

When building a :ref:`ref-classes-native` recipe, :term:`CC` is set to the
value of this variable by default.

The :term:`BUILD_CC` variable should not be set manually, and is rarely
used in recipes as :term:`CC` contains the appropriate value depending on
the context (native or target recipes). Exception be made for target
recipes that need to use the compiler from the build host at some point
during the build.
