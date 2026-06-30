Lists packages that should not be installed into an image. For
example::

   PACKAGE_EXCLUDE = "package_name package_name package_name ..."

You can set this variable globally in your ``local.conf`` file or you
can attach it to a specific image recipe by using the recipe name
override::

   PACKAGE_EXCLUDE:pn-target_image = "package_name"

If you choose to not install a package using this variable and some
other package is dependent on it (i.e. listed in a recipe's
:term:`RDEPENDS` variable), the OpenEmbedded build
system generates a fatal installation error. Because the build system
halts the process with a fatal error, you can use the variable with
an iterative development process to remove specific components from a
system.

This variable is supported for all packaging backends.

See the :term:`NO_RECOMMENDATIONS` and the
:term:`BAD_RECOMMENDATIONS` variables for
related information.
