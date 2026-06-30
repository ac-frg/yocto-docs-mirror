Points to the area that the OpenEmbedded build system uses to place
Debian packages that are ready to be used outside of the build
system. This variable applies only when :term:`PACKAGE_CLASSES` contains
":ref:`ref-classes-package_deb`".

The BitBake configuration file initially defines the
:term:`DEPLOY_DIR_DEB` variable as a sub-folder of
:term:`DEPLOY_DIR`::

   DEPLOY_DIR_DEB = "${DEPLOY_DIR}/deb"

The :ref:`ref-classes-package_deb` class uses the
:term:`DEPLOY_DIR_DEB` variable to make sure the
:term:`do_package_write_deb` task
writes Debian packages into the appropriate folder. For more
information on how packaging works, see the
":ref:`overview-manual/concepts:package feeds`" section
in the Yocto Project Overview and Concepts Manual.
