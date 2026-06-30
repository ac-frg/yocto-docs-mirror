Setting :term:`LICENSE_CREATE_PACKAGE` to "1" causes the OpenEmbedded
build system to create an extra package (i.e.
``${``\ :term:`PN`\ ``}-lic``) for each recipe and to add
those packages to the
:term:`RRECOMMENDS`\ ``:${PN}``.

The ``${PN}-lic`` package installs a directory in
``/usr/share/licenses`` named ``${PN}``, which is the recipe's base
name, and installs files in that directory that contain license and
copyright information (i.e. copies of the appropriate license files
from ``meta/common-licenses`` that match the licenses specified in
the :term:`LICENSE` variable of the recipe metadata
and copies of files marked in
:term:`LIC_FILES_CHKSUM` as containing
license text).

For related information on providing license text, see the
:term:`COPY_LIC_DIRS` variable, the
:term:`COPY_LIC_MANIFEST` variable, and the
":ref:`dev-manual/licenses:providing license text`"
section in the Yocto Project Development Tasks Manual.
