The parent directory used by the OpenEmbedded build system when
creating SDK output. The
:ref:`populate_sdk_base <ref-classes-populate-sdk-*>` class defines
the variable as follows::

   SDK_DIR = "${WORKDIR}/sdk"

.. note::

   The :term:`SDK_DIR` directory is a temporary directory as it is part of
   :term:`WORKDIR`. The final output directory is :term:`SDK_DEPLOY`.
