Specifies additional options for the image creation command that has
been specified in :term:`IMAGE_CMD`. When setting
this variable, use an override for the associated image type. Here is
an example::

   EXTRA_IMAGECMD:ext3 ?= "-i 4096"
