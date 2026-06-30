Defines the size in Kbytes for the generated image. The OpenEmbedded
build system determines the final size for the generated image using
an algorithm that takes into account the initial disk space used for
the generated image, a requested size for the image, and requested
additional free disk space to be added to the image. Programatically,
the build system determines the final size of the generated image as
follows::

   if (image-du * overhead) < rootfs-size:
       internal-rootfs-size = rootfs-size + xspace
   else:
       internal-rootfs-size = (image-du * overhead) + xspace
   where:
       image-du = Returned value of the du command on the image.
       overhead = IMAGE_OVERHEAD_FACTOR
       rootfs-size = IMAGE_ROOTFS_SIZE
       internal-rootfs-size = Initial root filesystem size before any modifications.
       xspace = IMAGE_ROOTFS_EXTRA_SPACE

See the :term:`IMAGE_OVERHEAD_FACTOR`
and :term:`IMAGE_ROOTFS_EXTRA_SPACE`
variables for related information.
