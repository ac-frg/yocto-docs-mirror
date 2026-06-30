The machine for which the SDK is built. In other words, the SDK is built
such that it runs on the target you specify with the :term:`SDKMACHINE`
value. The value points to a corresponding ``.conf`` file under
``conf/machine-sdk/`` in the enabled layers, for example ``aarch64``,
``i586``, ``i686``, ``ppc64``, ``ppc64le``, and ``x86_64`` are
:oe_git:`available in OpenEmbedded-Core </openembedded-core/tree/meta/conf/machine-sdk>`.

The variable defaults to :term:`BUILD_ARCH` so that SDKs are built for the
architecture of the build machine.

.. note::

   You cannot set the :term:`SDKMACHINE`
   variable in your distribution configuration file. If you do, the
   configuration will not take effect.
