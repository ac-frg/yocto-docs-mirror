Starts the image generation process. The :term:`do_image` task runs after
the OpenEmbedded build system has run the
:term:`do_rootfs` task during which packages are
identified for installation into the image and the root filesystem is
created, complete with post-processing.

The :term:`do_image` task performs pre-processing on the image through the
:term:`IMAGE_PREPROCESS_COMMAND` and
dynamically generates supporting :term:`do_image_* <do_image>` tasks as needed.

For more information on image creation, see the ":ref:`overview-manual/concepts:image generation`"
section in the Yocto Project Overview and Concepts Manual.
