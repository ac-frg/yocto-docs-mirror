Points to the area that the OpenEmbedded build system uses to place
RPM packages that are ready to be used outside of the build system.
This variable applies only when :term:`PACKAGE_CLASSES` contains
":ref:`ref-classes-package_rpm`".

The BitBake configuration file initially defines this variable as a
sub-folder of :term:`DEPLOY_DIR`::

   DEPLOY_DIR_RPM = "${DEPLOY_DIR}/rpm"

The :ref:`ref-classes-package_rpm` class uses the
:term:`DEPLOY_DIR_RPM` variable to make sure the
:term:`do_package_write_rpm` task
writes RPM packages into the appropriate folder. For more information
on how packaging works, see the
":ref:`overview-manual/concepts:package feeds`" section
in the Yocto Project Overview and Concepts Manual.
