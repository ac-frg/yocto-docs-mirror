Specifies the system, including the architecture and the operating
system, for which the build is occurring in the context of the
current recipe.

The OpenEmbedded build system automatically sets this variable based
on :term:`TARGET_ARCH`,
:term:`TARGET_VENDOR`, and
:term:`TARGET_OS` variables.

.. note::

   You do not need to set the :term:`TARGET_SYS` variable yourself.

Consider these two examples:

-  Given a native recipe on a 32-bit, x86 machine running Linux, the
   value is "i686-linux".

-  Given a recipe being built for a little-endian, MIPS target
   running Linux, the value might be "mipsel-linux".
