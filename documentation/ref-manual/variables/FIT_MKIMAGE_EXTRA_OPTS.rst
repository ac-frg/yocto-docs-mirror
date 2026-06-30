When inheriting the :ref:`ref-classes-kernel-fit-image`, the
:term:`FIT_MKIMAGE_EXTRA_OPTS` variable allows passing extra options to
``mkimage`` during FIT image generation, providing flexibility for platforms
that require additional ``mkimage`` arguments beyond the defaults.

For example::

   FIT_MKIMAGE_EXTRA_OPTS = "-B 8 -E"

This results in the ``mkimage`` command being invoked as:

.. parsed-literal::

   mkimage *-B 8 -E* -f fit-image.its fitImage
