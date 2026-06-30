Specifies the architecture-specific :manpage:`assembler <as(1)>` for the
build host, and its default definition is derived in part from
:term:`BUILD_PREFIX`::

   BUILD_AS = "${BUILD_PREFIX}as ${BUILD_AS_ARCH}"

When building a :ref:`ref-classes-native` recipe, :term:`AS` is set to the
value of this variable by default.

The :term:`BUILD_AS` variable should not be set manually, and is rarely
used in recipes as :term:`AS` contains the appropriate value depending on
the context (native or target recipes). Exception be made for target
recipes that need to use the :manpage:`assembler <as(1)>` from the build
host at some point during the build.
