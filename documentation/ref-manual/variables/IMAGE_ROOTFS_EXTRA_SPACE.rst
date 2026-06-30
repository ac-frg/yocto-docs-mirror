Defines additional free disk space created in the image in Kbytes. By
default, this variable is set to "0". This free disk space is added
to the image after the build system determines the image size as
described in :term:`IMAGE_ROOTFS_SIZE`.

This variable is particularly useful when you want to ensure that a
specific amount of free disk space is available on a device after an
image is installed and running. For example, to be sure 5 Gbytes of
free disk space is available, set the variable as follows::

   IMAGE_ROOTFS_EXTRA_SPACE = "5242880"

For example, the Yocto Project Build Appliance specifically requests
40 Gbytes of extra space with the line::

   IMAGE_ROOTFS_EXTRA_SPACE = "41943040"
