A list of packages replaced by a package. The package manager uses
this variable to determine which package should be installed to
replace other package(s) during an upgrade. In order to also have the
other package(s) removed at the same time, you must add the name of
the other package to the :term:`RCONFLICTS` variable.

As with all package-controlling variables, you must use this variable
in conjunction with a package name override. Here is an example::

   RREPLACES:${PN} = "other_package_being_replaced"

BitBake, which the OpenEmbedded build system uses, supports
specifying versioned replacements. Although the syntax varies
depending on the packaging format, BitBake hides these differences
from you. Here is the general syntax to specify versions with the
:term:`RREPLACES` variable::

   RREPLACES:${PN} = "package (operator version)"

For ``operator``, you can specify the following:

- =
- <
- >
- <=
- >=

For example, the following sets up a replacement using version 1.2
or greater of the package ``foo``::

    RREPLACES:${PN} = "foo (>= 1.2)"
