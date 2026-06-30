The :term:`SPDX_CONCLUDED_LICENSE` variable allows overriding the
``hasConcludedLicense`` object to individual SBOM packages. This can be
used when the license of a package was determined to be different than the
original license string value, after analysis.

This variable can be set in two ways:

-  For the entire recipe::

      SPDX_CONCLUDED_LICENSE = "MIT & Apache-2.0"

-  For an individual package produced by the recipe::

      SPDX_CONCLUDED_LICENSE:${PN} = "MIT & Apache-2.0"
