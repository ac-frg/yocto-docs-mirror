Defines a multiplier that the build system applies to the initial
image size for cases when the multiplier times the returned disk
usage value for the image is greater than the sum of
:term:`IMAGE_ROOTFS_SIZE` and :term:`IMAGE_ROOTFS_EXTRA_SPACE`. The result of
the multiplier applied to the initial image size creates free disk
space in the image as overhead. By default, the build process uses a
multiplier of 1.3 for this variable. This default value results in
30% free disk space added to the image when this method is used to
determine the final generated image size. You should be aware that
post install scripts and the package management system uses disk
space inside this overhead area. Consequently, the multiplier does
not produce an image with all the theoretical free disk space. See
:term:`IMAGE_ROOTFS_SIZE` for information on how the build system
determines the overall image size.

The default 30% free disk space typically gives the image enough room
to boot and allows for basic post installs while still leaving a
small amount of free disk space. If 30% free space is inadequate, you
can increase the default value. For example, the following setting
gives you 50% free space added to the image::

   IMAGE_OVERHEAD_FACTOR = "1.5"

Alternatively, you can ensure a specific amount of free disk space is
added to the image by using the :term:`IMAGE_ROOTFS_EXTRA_SPACE`
variable.

When using Wic tool, beware that a second overhead factor is also applied.
This overhead value is defined by the ``--overhead-factor`` option, which
defaults to "1.3" when omitted. See the
:ref:`ref-manual/kickstart:command: part or partition` chapter in
:doc:`/ref-manual/kickstart` for details.
