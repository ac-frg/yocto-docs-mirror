This option allows to add a description of the source files used to build
the host tools and the target packages, to the ``spdx.json`` files in
``tmp/deploy/spdx/MACHINE/recipes/`` under the :term:`Build Directory`.
As a consequence, the ``spdx.json`` files under the ``by-namespace`` and
``packages`` subdirectories in ``tmp/deploy/spdx/MACHINE`` are also
modified to include references to such source file descriptions.

Enable this option as follows::

   SPDX_INCLUDE_SOURCES = "1"

For SPDX 2.2 format (release 4.1 "langdale"), building
``core-image-minimal`` for the ``qemux86-64`` machine, enabling
this option multiplied the total size of the ``tmp/deploy/spdx``
directory by a factor of 3  (+291 MiB for this image),
and the size of the ``IMAGE-MACHINE.spdx.tar.zst`` in
``tmp/deploy/images/MACHINE`` by a factor of 130 (+15 MiB for this
image), compared to just using the :ref:`ref-classes-create-spdx` class
with no option.

With SPDX 3.0.1 JSON format, including source files significantly
increases the SBOM size (potentially by several gigabytes for typical
images).
