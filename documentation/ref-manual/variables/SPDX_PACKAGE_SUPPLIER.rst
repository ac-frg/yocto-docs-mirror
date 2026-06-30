The base variable name describing the agent who supplies the artifacts
produced by the build. Works identically to :term:`SPDX_IMAGE_SUPPLIER`
but applies to individual packages rather than the image SBOM.

Typically set in a distro :term:`configuration file` to apply globally
to all packages, or in a specific software recipe (or a ``.bbappend``)
to apply only to packages of that recipe. Recipe-level overrides
(``SPDX_PACKAGE_SUPPLIER:pn-<recipe>``) are also supported::

   SPDX_PACKAGE_SUPPLIER = "SPDX_PACKAGE_SUPPLIER"
   SPDX_PACKAGE_SUPPLIER_name = "Acme Corp"
   SPDX_PACKAGE_SUPPLIER_type = "organization"

See also :term:`SPDX_IMAGE_SUPPLIER` and :term:`SPDX_SDK_SUPPLIER`.
