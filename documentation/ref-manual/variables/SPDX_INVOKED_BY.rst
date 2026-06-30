The base variable name describing the agent that invoked the build.
Each ``Build`` object in the SPDX output is linked to this agent with an
``invokedBy`` relationship. Requires
:term:`SPDX_INCLUDE_BITBAKE_PARENT_BUILD` to be set to ``"1"``.

The sub-variables follow the same agent prefix convention as
:term:`SPDX_IMAGE_SUPPLIER`:

-  ``SPDX_INVOKED_BY_name``: display name of the invoking agent
-  ``SPDX_INVOKED_BY_type``: agent type, such as ``software`` for a CI system

Example (CI pipeline invoking the build)::

   SPDX_INCLUDE_BITBAKE_PARENT_BUILD = "1"
   SPDX_INVOKED_BY = "SPDX_INVOKED_BY"
   SPDX_INVOKED_BY_name = "GitLab CI"
   SPDX_INVOKED_BY_type = "software"

.. warning::

   Setting this variable will likely result in non-reproducible SPDX
   output, because the invoking agent identity varies across builds.

See also :term:`SPDX_INCLUDE_BITBAKE_PARENT_BUILD`,
:term:`SPDX_ON_BEHALF_OF`, and :term:`SPDX_BUILD_HOST`.
