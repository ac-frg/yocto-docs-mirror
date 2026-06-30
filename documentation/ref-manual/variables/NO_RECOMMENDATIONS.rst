Prevents installation of all "recommended-only" packages.
Recommended-only packages are packages installed only through the
:term:`RRECOMMENDS` variable). Setting the
:term:`NO_RECOMMENDATIONS` variable to "1" turns this feature on::

   NO_RECOMMENDATIONS = "1"

You can set this variable globally in your ``local.conf`` file or you
can attach it to a specific image recipe by using the recipe name
override::

   NO_RECOMMENDATIONS:pn-target_image = "1"

It is important to realize that if you choose to not install packages
using this variable and some other packages are dependent on them
(i.e. listed in a recipe's :term:`RDEPENDS`
variable), the OpenEmbedded build system ignores your request and
will install the packages to avoid dependency errors.

.. note::

   Some recommended packages might be required for certain system
   functionality, such as kernel modules. It is up to you to add
   packages with the :term:`IMAGE_INSTALL` variable.

This variable is supported for all packaging backends.

See the :term:`BAD_RECOMMENDATIONS` and
the :term:`PACKAGE_EXCLUDE` variables for
related information.
