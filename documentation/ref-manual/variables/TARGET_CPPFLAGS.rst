Specifies the flags to pass to the C pre-processor (i.e. to both the
C and the C++ compilers) when building for the target. When building
in the target context, :term:`CPPFLAGS` is set to the
value of this variable by default.

Additionally, the SDK's environment setup script sets the
:term:`CPPFLAGS` variable in the environment to the :term:`TARGET_CPPFLAGS`
value so that executables built using the SDK also have the flags
applied.
