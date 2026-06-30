The name of the output image symlink (which does not include
the version part as :term:`IMAGE_NAME` does). The default value
is derived using the :term:`IMAGE_BASENAME` and
:term:`IMAGE_MACHINE_SUFFIX` variables::

   IMAGE_LINK_NAME ?= "${IMAGE_BASENAME}${IMAGE_MACHINE_SUFFIX}"

.. note::

   It is possible to set this to "" to disable symlink creation,
   however, you also need to set :term:`IMAGE_NAME` to still have
   a reasonable value e.g.::

      IMAGE_LINK_NAME = ""
      IMAGE_NAME = "${IMAGE_BASENAME}${IMAGE_MACHINE_SUFFIX}${IMAGE_VERSION_SUFFIX}"
