When inheriting the :ref:`ref-classes-image` class directly or through the
:ref:`ref-classes-core-image` class, the :term:`IMAGE_OUTPUT_MANIFEST_DIR` points to
a directory that stores a manifest ``json`` file that lists what
images were created by various image creation tasks (as defined by the
:term:`IMAGE_FSTYPES` variable). It is set in the :ref:`ref-classes-image`
class as follows::

    IMAGE_OUTPUT_MANIFEST_DIR = "${WORKDIR}/deploy-image-output-manifest"
