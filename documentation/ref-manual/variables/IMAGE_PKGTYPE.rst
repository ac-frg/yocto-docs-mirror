Defines the package type (i.e. DEB, RPM or IPK) used by the
OpenEmbedded build system. The variable is defined appropriately by
one of the :ref:`ref-classes-package_deb`, :ref:`ref-classes-package_rpm`,
or :ref:`ref-classes-package_ipk` classes.

The :ref:`ref-classes-populate-sdk-*` and :ref:`ref-classes-image`
classes use the :term:`IMAGE_PKGTYPE` for packaging images and SDKs.

You should not set the :term:`IMAGE_PKGTYPE` manually. Rather, the
variable is set indirectly through the appropriate
:ref:`package_* <ref-classes-package>` class using the
:term:`PACKAGE_CLASSES` variable. The
OpenEmbedded build system uses the first package type (e.g. DEB, RPM,
or IPK) that appears with the variable
