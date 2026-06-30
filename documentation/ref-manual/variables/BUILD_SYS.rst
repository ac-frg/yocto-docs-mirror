Specifies the system, including the architecture and the operating
system, to use when building for the build host (i.e. when building
:ref:`ref-classes-native` recipes).

The OpenEmbedded build system automatically sets this variable based
on :term:`BUILD_ARCH`,
:term:`BUILD_VENDOR`, and
:term:`BUILD_OS`. You do not need to set the
:term:`BUILD_SYS` variable yourself.
