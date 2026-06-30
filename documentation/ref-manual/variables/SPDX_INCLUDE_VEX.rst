This option controls what `VEX <https://cyclonedx.org/capabilities/vex/>`__
information will be present in the output SPDX documents.

It can take three different values:

-  ``none``: disable all VEX data.

-  ``current`` (default): include VEX data for vulnerabilities not already
   fixed in the upstream source code.

-  ``all``: get all known historical vulnerabilities, including those
   already fixed upstream (warning: this can be large and slow).
