Lists "recommended-only" packages to not install. Recommended-only
packages are packages installed only through the
:term:`RRECOMMENDS` variable. You can prevent any
of these "recommended" packages from being installed by listing them
with the :term:`BAD_RECOMMENDATIONS` variable::

   BAD_RECOMMENDATIONS = "package_name package_name package_name ..."

You can set this variable globally in your ``local.conf`` file or you
can attach it to a specific image recipe by using the recipe name
override::

   BAD_RECOMMENDATIONS:pn-target_image = "package_name"

It is important to realize that if you choose to not install packages
using this variable and some other packages are dependent on them
(i.e. listed in a recipe's :term:`RDEPENDS`
variable), the OpenEmbedded build system ignores your request and
will install the packages to avoid dependency errors.

This variable is supported for the RPM and IPK packaging backends,
but not for DEB.

See the :term:`NO_RECOMMENDATIONS` and the
:term:`PACKAGE_EXCLUDE` variables for related
information.
