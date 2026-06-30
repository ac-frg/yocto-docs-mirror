Completes the image generation process. The :term:`do_image_complete` task
runs after the OpenEmbedded build system has run the
:term:`do_image` task during which image
pre-processing occurs and through dynamically generated :term:`do_image_*
<do_image>`
tasks the image is constructed.

The :term:`do_image_complete` task performs post-processing on the image
through the
:term:`IMAGE_POSTPROCESS_COMMAND`.

For more information on image creation, see the
":ref:`overview-manual/concepts:image generation`"
section in the Yocto Project Overview and Concepts Manual.
