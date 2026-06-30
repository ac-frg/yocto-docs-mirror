The manifest file for the image. This file lists all the installed
packages that make up the image. The file contains package
information on a line-per-package basis as follows::

    packagename packagearch version

The :ref:`rootfs-postcommands <ref-classes-rootfs*>` class defines the manifest
file as follows::

   IMAGE_MANIFEST = "${IMGDEPLOYDIR}/${IMAGE_NAME}${IMAGE_NAME_SUFFIX}.manifest"

The location is
derived using the :term:`IMGDEPLOYDIR`
and :term:`IMAGE_NAME` variables. You can find
information on how the image is created in the ":ref:`overview-manual/concepts:image generation`"
section in the Yocto Project Overview and Concepts Manual.
