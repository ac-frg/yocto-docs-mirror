Specifies a list of functions to call after the OpenEmbedded build
system has removed unnecessary packages. When runtime package
management is disabled in the image, several packages are removed
including ``base-passwd``, ``shadow``, and ``update-alternatives``.
You can specify functions separated by spaces::

   ROOTFS_POSTUNINSTALL_COMMAND += "function"

If you need to pass the root filesystem path to a command within a
function, you can use ``${IMAGE_ROOTFS}``, which points to the
directory that becomes the root filesystem image. See the
:term:`IMAGE_ROOTFS` variable for more
information.
