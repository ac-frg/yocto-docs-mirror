This variable cannot be set to a value in a config, it is a placeholder
for configuring the :term:`UBOOT_CONFIG` flow via flags::

   UBOOT_CONFIG_MAKE_OPTS[foo] = "OPT1=foo OPT2=2"
   UBOOT_CONFIG_MAKE_OPTS[bar] = "OPT1=bar"

It specifies a list of make command line options that are passed to the ``make`` command
during ``do_compile()``.

This option is not required and you only need to specify flag settings for
configs that need them.

For more information on how the :term:`UBOOT_CONFIG_MAKE_OPTS` is handled, see the
:ref:`ref-classes-uboot-config` class.
