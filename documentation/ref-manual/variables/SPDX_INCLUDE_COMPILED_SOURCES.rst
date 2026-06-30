This option allows the same as :term:`SPDX_INCLUDE_SOURCES` but including
only the sources used to compile the host tools and the target packages.
While :term:`SPDX_INCLUDE_SOURCES` includes all files in the source
directory as source file descriptions, :term:`SPDX_INCLUDE_COMPILED_SOURCES`
includes only the sources that are used to produce the binaries delivered
as packages. The source files that are not used during compilation are not
included in the SBOM. It uses debugsource information generated during
``do_package`` to filter out source files.

This enables an external tool to use the SPDX information to disregard
vulnerabilities that are not compiled in the packages.

Enable this option as follows::

   SPDX_INCLUDE_COMPILED_SOURCES = "1"

For SPDX 2.2 format (release 4.1 "langdale"), building
``core-image-minimal`` for the ``qemux86-64`` machine, this option
reduced the size of the ``tmp/deploy/spdx`` directory from 2GB to
1.6GB compared to :term:`SPDX_INCLUDE_SOURCES`, as it includes only
compiled objects without original source files.

With SPDX 3.0.1 JSON format, enabling this option includes both
compiled sources and original source files (same as
``SPDX_INCLUDE_SOURCES = "1"``), which significantly increases
the SBOM size. For example, with ``core-image-minimal`` on
``qemux86-64``, the uncompressed SBOM file can grow from hundreds
of megabytes to several gigabytes.
