Specifies the prefix used for the toolchain binary target tools.

Depending on the type of recipe and the build target,
:term:`TARGET_PREFIX` is set as follows:

-  For recipes building for the target machine, the value is
   "${:term:`TARGET_SYS`}-".

-  For native recipes, the build system sets the variable to the
   value of :term:`BUILD_PREFIX`.

-  For native SDK recipes (:ref:`ref-classes-nativesdk`),
   the build system sets the variable to the value of :term:`SDK_PREFIX`.
