The base variable name describing the build host on which the build is
running. The value must name a key from ``SPDX_IMPORTS``, allowing
the generated SPDX to reference externally defined host identity data.

Requires :term:`SPDX_INCLUDE_BITBAKE_PARENT_BUILD` to be set to ``"1"``.

.. warning::

   Setting this variable will result in non-reproducible SPDX output,
   because the build host identity may vary across builds.

See also :term:`SPDX_INCLUDE_BITBAKE_PARENT_BUILD`,
``SPDX_IMPORTS``, :term:`SPDX_INVOKED_BY`,
and :term:`SPDX_ON_BEHALF_OF`.
