Specifies additional paths from which the OpenEmbedded build system
gets source code. When the build system searches for source code, it
first tries the local download directory. If that location fails, the
build system tries locations defined by :term:`PREMIRRORS`, the upstream
source, and then locations specified by
:term:`MIRRORS` in that order.

The default value for :term:`PREMIRRORS` is defined in the
``meta/classes-global/mirrors.bbclass`` file in the core metadata layer.

Typically, you could add a specific server for the build system to
attempt before any others by adding something like the following to
the ``local.conf`` configuration file in the
:term:`Build Directory`::

   PREMIRRORS:prepend = "\
       git://.*/.* &YOCTO_DL_URL;/mirror/sources/ \
       ftp://.*/.* &YOCTO_DL_URL;/mirror/sources/ \
       http://.*/.* &YOCTO_DL_URL;/mirror/sources/ \
       https://.*/.* &YOCTO_DL_URL;/mirror/sources/"

These changes cause the
build system to intercept Git, FTP, HTTP, and HTTPS requests and
direct them to the ``http://`` sources mirror. You can use
``file://`` URLs to point to local directories or network shares as
well.

See the definition of this variable in the BitBake Manual for more
details: :term:`bitbake:PREMIRRORS`.
