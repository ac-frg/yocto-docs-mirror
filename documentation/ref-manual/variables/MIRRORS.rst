Specifies additional paths from which the OpenEmbedded build system
gets source code. When the build system searches for source code, it
first tries the local download directory. If that location fails, the
build system tries locations defined by
:term:`PREMIRRORS`, the upstream source, and then
locations specified by :term:`MIRRORS` in that order.

The default value for :term:`MIRRORS` is defined in the
``meta/classes-global/mirrors.bbclass`` file in the core metadata layer.

See the definition of this variable in the BitBake Manual for more
details: :term:`bitbake:MIRRORS`.
