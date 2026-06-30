The location used by the OpenEmbedded build system when creating SDK
output. The :ref:`populate_sdk_base <ref-classes-populate-sdk-*>`
class defines the variable as follows::

   SDK_DIR = "${WORKDIR}/sdk"
   SDK_OUTPUT = "${SDK_DIR}/image"
   SDK_DEPLOY = "${DEPLOY_DIR}/sdk"

.. note::

   The :term:`SDK_OUTPUT` directory is a temporary directory as it is part of
   :term:`WORKDIR` by way of :term:`SDK_DIR`. The final output directory is
   :term:`SDK_DEPLOY`.
