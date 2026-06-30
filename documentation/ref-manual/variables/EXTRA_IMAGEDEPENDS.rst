A list of recipes to build that do not provide packages for
installing into the root filesystem.

Sometimes a recipe is required to build the final image but is not
needed in the root filesystem. You can use the :term:`EXTRA_IMAGEDEPENDS`
variable to list these recipes and thus specify the dependencies. A
typical example is a required bootloader in a machine configuration.

.. note::

   To add packages to the root filesystem, see the various
   :term:`RDEPENDS` and :term:`RRECOMMENDS` variables.
