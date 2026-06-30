Specifies the flags to pass to the linker when building for the
target. When building in the target context,
:term:`LDFLAGS` is set to the value of this variable
by default.

Additionally, the SDK's environment setup script sets the
:term:`LDFLAGS` variable in the environment to the
:term:`TARGET_LDFLAGS` value so that executables built using the SDK also
have the flags applied.
