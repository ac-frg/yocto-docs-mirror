Specifies the toolchain selector. :term:`TCMODE` controls the
characteristics of the generated packages and images by telling the
OpenEmbedded build system which toolchain profile to use. By default,
the OpenEmbedded build system builds its own internal toolchain. The
variable's default value is "default", which uses that internal
toolchain.

.. note::

   If :term:`TCMODE` is set to a value other than "default", then it is your
   responsibility to ensure that the toolchain is compatible with the
   default toolchain. Using older or newer versions of these
   components might cause build problems. See
   :doc:`Release Information </migration-guides/index>` for your
   version of the Yocto Project, to find the specific components with
   which the toolchain must be compatible.

The :term:`TCMODE` variable is similar to :term:`TCLIBC`,
which controls the variant of the GNU standard C library (``libc``)
used during the build process: ``glibc`` or ``musl``.

With additional layers, it is possible to use a pre-compiled external
toolchain. One example is the Sourcery G++ Toolchain. The support for
this toolchain resides in the separate Mentor Graphics
``meta-sourcery`` layer at
https://github.com/MentorEmbedded/meta-sourcery/.

The layer's ``README`` file contains information on how to use the
Sourcery G++ Toolchain as an external toolchain. You will have to
add the layer to your ``bblayers.conf`` file and then set the
:term:`EXTERNAL_TOOLCHAIN` variable in your ``local.conf`` file to
the location of the toolchain.

The fundamentals used for this example apply to any external
toolchain. You can use ``meta-sourcery`` as a template for adding
support for other external toolchains.

In addition to toolchain configuration, you will also need a
corresponding toolchain recipe file. This recipe file needs to package
up any pre-built objects in the toolchain such as ``libgcc``,
``libstdcc++``, any locales, and ``libc``.
