Specifies the architecture-specific C++ compiler for the build host,
and its default definition is derived in part from :term:`BUILD_PREFIX`
and :term:`BUILD_CC_ARCH`::

   BUILD_CXX = "${CCACHE}${BUILD_PREFIX}g++ ${BUILD_CC_ARCH}"

When building a :ref:`ref-classes-native` recipe, :term:`CXX` is set to
the value of this variable by default.

The :term:`BUILD_CXX` variable should not be set manually, and is rarely
used in recipes as :term:`CXX` contains the appropriate value depending on
the context (native or target recipes). Exception be made for target
recipes that need to use the C++ compiler from the build host at some
point during the build.
