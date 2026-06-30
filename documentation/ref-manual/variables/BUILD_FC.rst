Specifies the Fortran compiler command for the build host, and its default
definition is derived in part from :term:`BUILD_PREFIX` and
:term:`BUILD_CC_ARCH`::

   BUILD_FC = "${BUILD_PREFIX}gfortran ${BUILD_CC_ARCH}"

When building a :ref:`ref-classes-native` recipe, :term:`FC` is set to the
value of this variable by default.

The :term:`BUILD_FC` variable should not be set manually, and is rarely
used in recipes as :term:`FC` contains the appropriate value depending on
the context (native or target recipes). Exception be made for target
recipes that need to use the Fortran compiler from the build host at some
point during the build.
