The list of packages that conflict with packages. Note that packages
will not be installed if conflicting packages are not first removed.

Like all package-controlling variables, you must always use them in
conjunction with a package name override. Here is an example::

   RCONFLICTS:${PN} = "another_conflicting_package_name"

BitBake, which the OpenEmbedded build system uses, supports
specifying versioned dependencies. Although the syntax varies
depending on the packaging format, BitBake hides these differences
from you. Here is the general syntax to specify versions with the
:term:`RCONFLICTS` variable::

   RCONFLICTS:${PN} = "package (operator version)"

For ``operator``, you can specify the following:

- =
- <
- >
- <=
- >=

For example, the following sets up a dependency on version 1.2 or
greater of the package ``foo``::

   RCONFLICTS:${PN} = "foo (>= 1.2)"
