Load address for the loadables defined in :term:`FIT_LOADABLES`; the
value will be used for the ``load`` property of the loadable.
This is mandatory for each loadable.

This variable cannot be used directly, but only defining flags on it.

Example::

   FIT_LOADABLES = "foo"
   FIT_LOADABLE_LOADADDRESS[foo] = "0x80230000"
