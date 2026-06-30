Specifies the formats the OpenEmbedded build system uses during the
build when creating the root filesystem. For example, setting
:term:`IMAGE_FSTYPES` as follows causes the build system to create root
filesystems using two formats: ``.ext3`` and ``.tar.bz2``::

   IMAGE_FSTYPES = "ext3 tar.bz2"

For the complete list of supported image formats from which you can
choose, see :term:`IMAGE_TYPES`.

.. note::

   -  If an image recipe uses the "inherit image" line and you are
      setting :term:`IMAGE_FSTYPES` inside the recipe, you must set
      :term:`IMAGE_FSTYPES` prior to using the "inherit image" line.

   -  Due to the way the OpenEmbedded build system processes this
      variable, you cannot update its contents by using ``:append``
      or ``:prepend``. You must use the ``+=`` operator to add one or
      more options to the :term:`IMAGE_FSTYPES` variable.
