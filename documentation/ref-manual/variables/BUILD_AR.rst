Specifies the architecture-specific :manpage:`archiver <ar(1)>` for the
build host, and its default definition is derived in part from
:term:`BUILD_PREFIX`::

   BUILD_AR = "${BUILD_PREFIX}ar"

When building a :ref:`ref-classes-native` recipe, :term:`AR` is set to the
value of this variable by default.

The :term:`BUILD_AR` variable should not be set manually, and is rarely
used in recipes as :term:`AR` contains the appropriate value depending on
the context (native or target recipes). Exception be made for target
recipes that need to use the :manpage:`archiver <ar(1)>` from the build
host at some point during the build.
