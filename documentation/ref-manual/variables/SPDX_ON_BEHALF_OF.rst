The base variable name describing the agent on whose behalf the invoking
agent (:term:`SPDX_INVOKED_BY`) is running the build. Requires
:term:`SPDX_INCLUDE_BITBAKE_PARENT_BUILD` to be set to ``"1"``.
Has no effect if :term:`SPDX_INVOKED_BY` is not also set.

The sub-variables follow the same agent prefix convention as
:term:`SPDX_IMAGE_SUPPLIER`:

-  ``SPDX_ON_BEHALF_OF_name``: display name of the commissioning agent
-  ``SPDX_ON_BEHALF_OF_type``: agent type, such as ``organization``

Example (CI system building on behalf of a customer organization)::

   SPDX_INCLUDE_BITBAKE_PARENT_BUILD = "1"
   SPDX_INVOKED_BY = "SPDX_INVOKED_BY"
   SPDX_INVOKED_BY_name = "GitLab CI"
   SPDX_INVOKED_BY_type = "software"
   SPDX_ON_BEHALF_OF = "SPDX_ON_BEHALF_OF"
   SPDX_ON_BEHALF_OF_name = "Acme Corp"
   SPDX_ON_BEHALF_OF_type = "organization"

.. warning::

   Setting this variable will likely result in non-reproducible SPDX
   output, because the agent identity varies across builds.

See also :term:`SPDX_INCLUDE_BITBAKE_PARENT_BUILD`,
:term:`SPDX_INVOKED_BY`, and :term:`SPDX_BUILD_HOST`.
