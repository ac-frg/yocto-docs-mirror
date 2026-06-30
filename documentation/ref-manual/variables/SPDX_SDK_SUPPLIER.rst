The base variable name describing the agent who supplies the SDK SBOM.
When set, the supplier is attached to all root elements of the SDK
SBOM using the ``suppliedBy`` property.

Works identically to :term:`SPDX_IMAGE_SUPPLIER` but applies to SDK
builds. This includes image-based SDKs produced by
``bitbake <image> -c populate_sdk`` as well as toolchain SDKs produced
by ``bitbake meta-toolchain``.

Typically set in the image recipe or in a :term:`configuration file`.

If not set, no supplier information is added to the SDK SBOM.

See also :term:`SPDX_IMAGE_SUPPLIER` and :term:`SPDX_PACKAGE_SUPPLIER`.
