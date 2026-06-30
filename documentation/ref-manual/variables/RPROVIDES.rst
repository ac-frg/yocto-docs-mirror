A list of package name aliases that a package also provides. These
aliases are useful for satisfying runtime dependencies of other
packages both during the build and on the target (as specified by
:term:`RDEPENDS`).

.. note::

   A package's own name is implicitly already in its :term:`RPROVIDES` list.

As with all package-controlling variables, you must always use the
variable in conjunction with a package name override. Here is an
example::

   RPROVIDES:${PN} = "widget-abi-2"
