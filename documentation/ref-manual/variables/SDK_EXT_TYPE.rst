Controls whether or not shared state artifacts are copied into the
extensible SDK. The default value of "full" copies all of the
required shared state artifacts into the extensible SDK. The value
"minimal" leaves these artifacts out of the SDK.

.. note::

   If you set the variable to "minimal", you need to ensure
   :term:`SSTATE_MIRRORS` is set in the SDK's configuration to enable the
   artifacts to be fetched as needed.
