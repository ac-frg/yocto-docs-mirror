When inheriting the :ref:`ref-classes-sbom-cve-check` class, this
variable controls whether to show warnings when CVEs with the
``Unpatched`` status are found. Example output:

.. code-block:: text

   WARNING: core-image-minimal-1.0-r0 do_sbom_cve_check: glibc-2.43+git: Found unpatched CVEs: CVE-2010-4756

Set to "1" to show the warnings, "0" otherwise.

See :doc:`/security-manual/vulnerabilities` for more information.
