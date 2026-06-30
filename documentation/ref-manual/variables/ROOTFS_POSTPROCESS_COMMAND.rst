Specifies a list of functions to call once the OpenEmbedded build
system has created the root filesystem. You can specify functions
separated by spaces::

   ROOTFS_POSTPROCESS_COMMAND += "function"

If you need to pass the root filesystem path to a command within a
function, you can use ``${IMAGE_ROOTFS}``, which points to the
directory that becomes the root filesystem image. See the
:term:`IMAGE_ROOTFS` variable for more
information.
