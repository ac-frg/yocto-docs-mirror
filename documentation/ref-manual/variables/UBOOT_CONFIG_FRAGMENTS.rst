This variable cannot be set to a value in a config, it is a placeholder
for configuring the :term:`UBOOT_CONFIG` flow via flags::

   UBOOT_CONFIG_FRAGMENTS[foo] = "frag1 frag2"
   UBOOT_CONFIG_FRAGMENTS[bar] = "frag3"

It specifies a list of fragments from the source tree that should be combined
with the defconfig from :term:`UBOOT_CONFIG` that are used during ``do_configure()``
to configure the build.  These fragments are located in same
``${S}/configs/`` directory as the defconfig.

This option is not required and you only need to specify it for
configs that need them.

For more information on how the :term:`UBOOT_CONFIG_FRAGMENTS` variable is handled, see the
:ref:`ref-classes-uboot-config` class.
