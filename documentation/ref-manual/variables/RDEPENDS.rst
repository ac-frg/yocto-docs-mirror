Lists runtime dependencies of a package. These dependencies are other
packages that must be installed in order for the package to function
correctly. As an example, the following assignment declares that the
package ``foo`` needs the packages ``bar`` and ``baz`` to be
installed::

   RDEPENDS:foo = "bar baz"

The most common types of package
runtime dependencies are automatically detected and added. Therefore,
most recipes do not need to set :term:`RDEPENDS`. For more information,
see the
":ref:`overview-manual/concepts:automatically added runtime dependencies`"
section in the Yocto Project Overview and Concepts Manual.

The practical effect of the above :term:`RDEPENDS` assignment is that
``bar`` and ``baz`` will be declared as dependencies inside the
package ``foo`` when it is written out by one of the
:term:`do_package_write_* <do_package_write_deb>` tasks.
Exactly how this is done depends on which package format is used,
which is determined by
:term:`PACKAGE_CLASSES`. When the
corresponding package manager installs the package, it will know to
also install the packages on which it depends.

To ensure that the packages ``bar`` and ``baz`` get built, the
previous :term:`RDEPENDS` assignment also causes a task dependency to be
added. This dependency is from the recipe's
:term:`do_build` (not to be confused with
:term:`do_compile`) task to the
:term:`do_package_write_* <do_package_write_deb>` task of the recipes that build ``bar`` and
``baz``.

The names of the packages you list within :term:`RDEPENDS` must be the
names of other packages --- they cannot be recipe names. Although
package names and recipe names usually match, the important point
here is that you are providing package names within the :term:`RDEPENDS`
variable. For an example of the default list of packages created from
a recipe, see the :term:`PACKAGES` variable.

Because the :term:`RDEPENDS` variable applies to packages being built,
you should always use the variable in a form with an attached package
name (remember that a single recipe can build multiple packages). For
example, suppose you are building a development package that depends
on the ``perl`` package. In this case, you would use the following
:term:`RDEPENDS` statement::

   RDEPENDS:${PN}-dev += "perl"

In the example,
the development package depends on the ``perl`` package. Thus, the
:term:`RDEPENDS` variable has the ``${PN}-dev`` package name as part of
the variable.

.. note::

   ``RDEPENDS:${PN}-dev`` includes ``${``\ :term:`PN`\ ``}``
   by default. This default is set in the BitBake configuration file
   (``meta/conf/bitbake.conf``). Be careful not to accidentally remove
   ``${PN}`` when modifying ``RDEPENDS:${PN}-dev``. Use the "+=" operator
   rather than the "=" operator.

The package names you use with :term:`RDEPENDS` must appear as they would
in the :term:`PACKAGES` variable. The :term:`PKG` variable
allows a different name to be used for the final package (e.g. the
:ref:`ref-classes-debian` class uses this to rename
packages), but this final package name cannot be used with
:term:`RDEPENDS`, which makes sense as :term:`RDEPENDS` is meant to be
independent of the package format used.

BitBake, which the OpenEmbedded build system uses, supports
specifying versioned dependencies. Although the syntax varies
depending on the packaging format, BitBake hides these differences
from you. Here is the general syntax to specify versions with the
:term:`RDEPENDS` variable::

   RDEPENDS:${PN} = "package (operator version)"

For ``operator``, you can specify the following:

- =
- <
- >
- <=
- >=

For version, provide the version number.

.. note::

   You can use :term:`EXTENDPKGV` to provide a full package version
   specification.

For example, the following sets up a dependency on version 1.2 or
greater of the package ``foo``::

   RDEPENDS:${PN} = "foo (>= 1.2)"

For information on build-time dependencies, see the :term:`DEPENDS`
variable. You can also see the
":ref:`bitbake-user-manual/bitbake-user-manual-metadata:tasks`" and
":ref:`bitbake-user-manual/bitbake-user-manual-execution:dependencies`" sections in the
BitBake User Manual for additional information on tasks and dependencies.
