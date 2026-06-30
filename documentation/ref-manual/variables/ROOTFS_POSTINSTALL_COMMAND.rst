Specifies a list of functions to call after the OpenEmbedded build
system has installed packages. You can specify functions separated by
spaces::

   ROOTFS_POSTINSTALL_COMMAND += "function"

If you need to pass the root filesystem path to a command within a
function, you can use ``${IMAGE_ROOTFS}``, which points to the
directory that becomes the root filesystem image. See the
:term:`IMAGE_ROOTFS` variable for more
information.
