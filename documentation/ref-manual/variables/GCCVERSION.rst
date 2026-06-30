Specifies the default version of the GNU C Compiler (GCC) used for
compilation. By default, :term:`GCCVERSION` is set to "8.x" in the
``meta/conf/distro/include/tcmode-default.inc`` include file::

   GCCVERSION ?= "8.%"

You can override this value by setting it in a
configuration file such as the ``local.conf``.
