Entry point for the loadables defined in :term:`FIT_LOADABLES`; the value
will be used for the ``entry`` property of the loadable.
If no value is defined for a specific loadable, the ``entry`` property
will be omitted.

This variable cannot be used directly, but only defining flags on it.

Example::

   FIT_LOADABLES = "foo"
   FIT_LOADABLE_ENTRYPOINT[foo] = "0x80234000"
