When inheriting the :ref:`ref-classes-sbom-cve-check` class, this variable
holds the list of variables that declare export files to generate.

Each variable must have a ``type`` and an ``ext`` flag set:

-  The ``type`` flag contains the value that is passed to the
   ``--export-type`` command line argument of ``sbom-cve-check``.

-  The ``ext`` flag contains the filename extension (suffix). The output
   filename is going will be ``${IMAGE_NAME}${ext}``.

For example::

   SBOM_CVE_CHECK_EXPORT_VARS = "SBOM_CVE_CHECK_EXPORT_SPDX3"
   SBOM_CVE_CHECK_EXPORT_SPDX3[type] = "spdx3"
   SBOM_CVE_CHECK_EXPORT_SPDX3[ext] = ".sbom-cve-check.spdx.json"
