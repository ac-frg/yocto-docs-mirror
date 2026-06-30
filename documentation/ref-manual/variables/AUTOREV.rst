When :term:`SRCREV` is set to the value of this variable, it specifies to
use the latest source revision in the repository. Here is an example::

   SRCREV = "${AUTOREV}"

If you use the previous statement to retrieve the latest version of
software, you need to make sure :term:`PV` contains the ``+`` sign so
:term:`bitbake` includes source control information to :term:`PKGV` when
packaging the recipe. For example::

   PV = "6.10.y+git"

For more information see the
":ref:`dev-manual/packages:automatically incrementing a package version number`"
section in the Yocto Project Development Tasks Manual.
