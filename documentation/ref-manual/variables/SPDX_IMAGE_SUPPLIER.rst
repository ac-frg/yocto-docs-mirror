The name of an agent variable prefix describing the organization or
person who supplies the image SBOM. When set, the supplier is attached
to all root elements of the image SBOM using the ``suppliedBy`` property.

The value of this variable is the base prefix used to look up the
agent's details. The following sub-variables are read using that prefix:

-  ``<PREFIX>_name``: display name of the supplier (required)
-  ``<PREFIX>_type``: agent type: ``organization``, ``person``,
   ``software``, or ``agent`` (optional, defaults to ``agent``)
-  ``<PREFIX>_comment``: free-text comment (optional)
-  ``<PREFIX>_id_email``: contact e-mail address (optional)

The simplest approach is to use the variable itself as its own prefix,
so the sub-variable names follow directly from
``SPDX_IMAGE_SUPPLIER``.

Example (set in the image recipe or in a :term:`configuration file`)::

   SPDX_IMAGE_SUPPLIER = "SPDX_IMAGE_SUPPLIER"
   SPDX_IMAGE_SUPPLIER_name = "Acme Corp"
   SPDX_IMAGE_SUPPLIER_type = "organization"

Alternatively, you can use any other prefix name, which is useful for
sharing an agent definition across multiple supplier variables::

   MY_COMPANY_name = "Acme Corp"
   MY_COMPANY_type = "organization"
   SPDX_IMAGE_SUPPLIER = "MY_COMPANY"
   SPDX_SDK_SUPPLIER = "MY_COMPANY"

If not set, no supplier information is added to the image SBOM.

See also :term:`SPDX_PACKAGE_SUPPLIER` and :term:`SPDX_SDK_SUPPLIER`.
