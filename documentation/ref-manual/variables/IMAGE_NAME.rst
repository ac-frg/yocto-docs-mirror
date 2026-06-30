The name of the output image files minus the extension. By default
this variable is set using the :term:`IMAGE_LINK_NAME`, and
:term:`IMAGE_VERSION_SUFFIX` variables::

   IMAGE_NAME ?= "${IMAGE_LINK_NAME}${IMAGE_VERSION_SUFFIX}"
