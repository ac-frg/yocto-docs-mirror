Operating system for the loadables defined in :term:`FIT_LOADABLES`; the
value will be used for the ``os`` property of the loadable.
If no value is defined for a specific loadable, the ``os`` property will
be set to ``linux``.

This variable cannot be used directly, but only defining flags on it.

Example::

   FIT_LOADABLES = "foo"
   FIT_LOADABLE_OS[foo] = "linux"
