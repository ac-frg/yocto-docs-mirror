When set to ``"1"``, the SPDX output will include a ``Build`` object
representing the parent :term:`BitBake` invocation. This allows consumers
of the SBOM to trace which CI/CD job or orchestration system triggered
the build.

This variable is required for :term:`SPDX_INVOKED_BY`,
:term:`SPDX_ON_BEHALF_OF`, and :term:`SPDX_BUILD_HOST` to have any
effect.

.. warning::

   Enabling this variable will result in non-reproducible SPDX output,
   because the build invocation identity changes with every run.

Enable as follows::

   SPDX_INCLUDE_BITBAKE_PARENT_BUILD = "1"

See also :term:`SPDX_BUILD_HOST`, :term:`SPDX_INVOKED_BY`,
and :term:`SPDX_ON_BEHALF_OF`.
