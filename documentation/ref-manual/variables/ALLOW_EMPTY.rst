Specifies whether to produce an output package even if it is empty.
By default, BitBake does not produce empty packages. This default
behavior can cause issues when there is an
:term:`RDEPENDS` or some other hard runtime
requirement on the existence of the package.

Like all package-controlling variables, you must always use them in
conjunction with a package name override, as in::

   ALLOW_EMPTY:${PN} = "1"
   ALLOW_EMPTY:${PN}-dev = "1"
   ALLOW_EMPTY:${PN}-staticdev = "1"
