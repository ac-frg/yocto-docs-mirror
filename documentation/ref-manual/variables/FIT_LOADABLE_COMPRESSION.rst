Compression type for the loadables defined in :term:`FIT_LOADABLES`; the
value will be used for the ``compression`` property of the loadable.
If no value is defined for a specific loadable, its ``compression``
property will be set to ``none``.

This variable cannot be used directly, but only defining flags on it.

Example::

   FIT_LOADABLES = "foo"
   FIT_LOADABLE_COMPRESSION[foo] = "gzip"

.. note::

   The binary should already be compressed, as no compression is
   performed by the :ref:`ref-classes-kernel-fit-image` class.
