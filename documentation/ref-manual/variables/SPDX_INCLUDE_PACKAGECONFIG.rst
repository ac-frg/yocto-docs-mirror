This option allows exporting a recipe's :term:`PACKAGECONFIG`
features into the recipe's SPDX document. Each feature is
recorded as a ``DictionaryEntry`` with key
``PACKAGECONFIG:<feature>`` and value ``enabled`` or
``disabled``, depending on whether the feature is active in
the current build.

.. note::

   This variable only has effect when using the SPDX 3.0 output
   format (see :ref:`ref-classes-create-spdx`).

Enable this option as follows::

   SPDX_INCLUDE_PACKAGECONFIG = "1"

When enabled, the build-time configuration of each recipe is
captured in the SPDX document, improving transparency,
reproducibility, and security auditing. It allows consumers of
the SPDX SBOM to determine which optional features were
enabled or disabled in a given build.
