Description for the loadables defined in :term:`FIT_LOADABLES`; the value
will be used for the ``description`` property of the loadable.
If no value is defined for a specific loadable, its description will be
set to the loadable name followed by a space plus the string ``loadable``.

This variable cannot be used directly, but only defining flags on it.

Example::

   FIT_LOADABLES = "foo"
   FIT_LOADABLE_DESCRIPTION[foo] = "Foo firmware binary"
