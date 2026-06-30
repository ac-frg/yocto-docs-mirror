Points to the area that the OpenEmbedded build system uses to place
images and other associated output files that are ready to be
deployed onto the target machine. The directory is machine-specific
as it contains the ``${MACHINE}`` name. By default, this directory
resides within the :term:`Build Directory` as
``${DEPLOY_DIR}/images/${MACHINE}/``.

It must not be used directly in recipes when deploying files. Instead,
it's only useful when a recipe needs to "read" a file already deployed
by a dependency. So, it should be filled with the contents of
:term:`DEPLOYDIR` by the :ref:`ref-classes-deploy` class or with the
contents of :term:`IMGDEPLOYDIR` by the :ref:`ref-classes-image` class.

For more information on the structure of the :term:`Build Directory`, see
":ref:`ref-manual/structure:the build directory --- ``build/```" section.
For more detail on the contents of the ``deploy`` directory, see the
":ref:`overview-manual/concepts:images`" and
":ref:`overview-manual/concepts:application development sdk`" sections both in
the Yocto Project Overview and Concepts Manual.
