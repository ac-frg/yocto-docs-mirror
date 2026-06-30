A list of packages that extends the usability of a package being
built. The package being built does not depend on this list of
packages in order to successfully build, but rather uses them for
extended usability. To specify runtime dependencies for packages, see
the :term:`RDEPENDS` variable.

The package manager will automatically install the :term:`RRECOMMENDS`
list of packages when installing the built package. However, you can
prevent listed packages from being installed by using the
:term:`BAD_RECOMMENDATIONS`,
:term:`NO_RECOMMENDATIONS`, and
:term:`PACKAGE_EXCLUDE` variables.

Packages specified in :term:`RRECOMMENDS` need not actually be produced.
However, there must be a recipe providing each package, either
through the :term:`PACKAGES` or
:term:`PACKAGES_DYNAMIC` variables or the
:term:`RPROVIDES` variable, or an error will occur
during the build. If such a recipe does exist and the package is not
produced, the build continues without error.

Because the :term:`RRECOMMENDS` variable applies to packages being built,
you should always attach an override to the variable to specify the
particular package whose usability is being extended. For example,
suppose you are building a development package that is extended to
support wireless functionality. In this case, you would use the
following::

   RRECOMMENDS:${PN}-dev += "wireless_package_name"

In the
example, the package name (``${PN}-dev``) must appear as it would in
the :term:`PACKAGES` namespace before any renaming of the output package
by classes such as :ref:`ref-classes-debian`.

BitBake, which the OpenEmbedded build system uses, supports
specifying versioned recommends. Although the syntax varies depending
on the packaging format, BitBake hides these differences from you.
Here is the general syntax to specify versions with the
:term:`RRECOMMENDS` variable::

   RRECOMMENDS:${PN} = "package (operator version)"

For ``operator``, you can specify the following:

- =
- <
- >
- <=
- >=

For example, the following sets up a recommend on version 1.2 or
greater of the package ``foo``::

   RRECOMMENDS:${PN} = "foo (>= 1.2)"
