Type for the loadables defined in :term:`FIT_LOADABLES`; the value will
be used for the ``type`` property of the loadable.
If no value is defined for a specific loadable, the ``type`` property
will be set to ``firmware``.

This variable cannot be used directly, but only defining flags on it.

Example::

   FIT_LOADABLES = "foo"
   FIT_LOADABLE_TYPE[foo] = "firmware"
