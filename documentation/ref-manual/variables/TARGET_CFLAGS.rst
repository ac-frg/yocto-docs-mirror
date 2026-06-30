Specifies the flags to pass to the C compiler when building for the
target. When building in the target context,
:term:`CFLAGS` is set to the value of this variable by
default.

Additionally, the SDK's environment setup script sets the :term:`CFLAGS`
variable in the environment to the :term:`TARGET_CFLAGS` value so that
executables built using the SDK also have the flags applied.
