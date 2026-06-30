A space-separated list of ``domain:purl_type`` mappings to configure PURL
(Package URLs) generation for Git source downloads.

For example, adding ``gitlab.example.com:pkg:gitlab`` to this variable
will map repositories hosted on "gitlab.example.com" to the ``pkg:gitlab``
PURL type.

See also the :term:`SPDX_PACKAGE_URLS` variable for more information on
PURLs.
