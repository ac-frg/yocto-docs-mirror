Specifies the :manpage:`linker <ld(1)>` command to be used for the build
host when the C compiler is being used as the linker, and its default
definition is derived in part from :term:`BUILD_PREFIX` and
:term:`BUILD_CC_ARCH`::

   BUILD_CCLD = "${BUILD_PREFIX}gcc ${BUILD_CC_ARCH}"

When building a :ref:`ref-classes-native` recipe, :term:`CCLD` is set to
the value of this variable by default.

The :term:`BUILD_CCLD` variable should not be set manually, and is rarely
used in recipes as :term:`CCLD` contains the appropriate value depending on
the context (native or target recipes). Exception be made for target
recipes that need to use the :manpage:`linker <ld(1)>` from the build host
at some point during the build.
