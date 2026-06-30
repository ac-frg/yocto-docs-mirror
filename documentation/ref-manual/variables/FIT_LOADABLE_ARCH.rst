Architecture the loadables defined in :term:`FIT_LOADABLES`; the value
will be used for the ``arch`` property of the loadable.
If no value is defined for a specific loadable, the kernel architecture
will be used.

This variable cannot be used directly, but only defining flags on it.

Example::

   FIT_LOADABLES = "foo"
   FIT_LOADABLE_ARCH[foo] = "arm"
