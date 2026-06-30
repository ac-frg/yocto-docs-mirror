When inheriting the :ref:`ref-classes-image` class directly or through the
:ref:`ref-classes-core-image` class, the :term:`IMGMANIFESTDIR` setting
points to a temporary area that stores manifest ``json`` files, that list
what images were created by various images creation tasks (as defined by
the :term:`IMAGE_FSTYPES` variable). It is set in the
:ref:`ref-classes-image` class as follows::

    IMGMANIFESTDIR = "${WORKDIR}/image-task-manifest"
