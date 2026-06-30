Points to the area that the OpenEmbedded build system uses to place
IPK packages that are ready to be used outside of the build system.
This variable applies only when :term:`PACKAGE_CLASSES` contains
":ref:`ref-classes-package_ipk`".

The BitBake configuration file initially defines this variable as a
sub-folder of :term:`DEPLOY_DIR`::

   DEPLOY_DIR_IPK = "${DEPLOY_DIR}/ipk"

The :ref:`ref-classes-package_ipk` class uses the :term:`DEPLOY_DIR_IPK`
variable to make sure the :term:`do_package_write_ipk` task
writes IPK packages into the appropriate folder. For more information
on how packaging works, see the
":ref:`overview-manual/concepts:package feeds`" section
in the Yocto Project Overview and Concepts Manual.
