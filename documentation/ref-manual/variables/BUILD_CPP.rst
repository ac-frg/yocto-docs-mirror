Specifies the C preprocessor command (to both the C and the C++ compilers)
when building for the build host, and its default definition is derived in
part from :term:`BUILD_PREFIX` and :term:`BUILD_CC_ARCH`::

   BUILD_CPP = "${BUILD_PREFIX}gcc ${BUILD_CC_ARCH} -E"

When building a :ref:`ref-classes-native` recipe, :term:`CPP` is set to
the value of this variable by default.

The :term:`BUILD_CPP` variable should not be set manually, and is rarely
used in recipes as :term:`CPP` contains the appropriate value depending on
the context (native or target recipes). Exception be made for target
recipes that need to use the preprocessor from the build host at some
point during the build.
