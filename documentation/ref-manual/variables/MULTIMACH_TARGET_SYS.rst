Uniquely identifies the type of the target system for which packages
are being built. This variable allows output for different types of
target systems to be put into different subdirectories of the same
output directory.

The default value of this variable is::

   ${PACKAGE_ARCH}${TARGET_VENDOR}-${TARGET_OS}

Some classes (e.g.  :ref:`ref-classes-cross-canadian`) modify the
:term:`MULTIMACH_TARGET_SYS` value.

See the :term:`STAMP` variable for an example. See the
:term:`STAGING_DIR_TARGET` variable for more information.
