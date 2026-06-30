When inheriting the :ref:`ref-classes-deploy` class, the
:term:`DEPLOYDIR` points to a temporary work area for deployed files that
is set in the :ref:`ref-classes-deploy` class as follows::

   DEPLOYDIR = "${WORKDIR}/deploy-${PN}"

Recipes inheriting the :ref:`ref-classes-deploy` class should copy files to be
deployed into :term:`DEPLOYDIR`, and the class will take care of copying
them into :term:`DEPLOY_DIR_IMAGE`
afterwards.

.. warning::

   Do not confuse this variable with the similarly-named
   :term:`DEPLOY_DIR` variable.
