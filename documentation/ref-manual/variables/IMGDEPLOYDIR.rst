When inheriting the :ref:`ref-classes-image` class directly or
through the :ref:`ref-classes-core-image` class, the
:term:`IMGDEPLOYDIR` points to a temporary work area for deployed files
that is set in the ``image`` class as follows::

   IMGDEPLOYDIR = "${WORKDIR}/deploy-${PN}-image-complete"

Recipes inheriting the :ref:`ref-classes-image` class should copy
files to be deployed into :term:`IMGDEPLOYDIR`, and the class will take
care of copying them into :term:`DEPLOY_DIR_IMAGE` afterwards.
