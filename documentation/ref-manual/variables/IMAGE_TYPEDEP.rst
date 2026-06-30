Specifies a dependency from one image type on another. Here is an
example from the :ref:`ref-classes-image-live` class::

   IMAGE_TYPEDEP:live = "ext3"

In the previous example, the variable ensures that when "live" is
listed with the :term:`IMAGE_FSTYPES` variable,
the OpenEmbedded build system produces an ``ext3`` image first since
one of the components of the live image is an ``ext3`` formatted
partition containing the root filesystem.
