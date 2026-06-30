This variable controls the toolchain used for compiling
:ref:`ref-classes-native` recipes.

This variable should be set globally from a :term:`configuration file`.

See :term:`PREFERRED_TOOLCHAIN_TARGET` for more details on the possible
values for this variable.

A recipe that does not support the toolchain specified by
:term:`PREFERRED_TOOLCHAIN_NATIVE` can override it locally with
:term:`TOOLCHAIN_NATIVE`.
