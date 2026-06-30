A list of machine-specific packages to install as part of the image
being built that are not essential for the machine to boot. However,
the build process for more fully-featured images depends on the
packages being present.

This variable affects all images based on ``packagegroup-base``,
which does not include the ``core-image-minimal`` or
``core-image-full-cmdline`` images.

The variable is similar to the :term:`MACHINE_EXTRA_RRECOMMENDS` variable
with the exception that the image being built has a build dependency
on the variable's list of packages. In other words, the image will
not build if a file in this list is not found.

An example is a machine that has WiFi capability but is not essential
for the machine to boot the image. However, if you are building a
more fully-featured image, you want to enable the WiFi. The package
containing the firmware for the WiFi hardware is always expected to
exist, so it is acceptable for the build process to depend upon
finding the package. In this case, assuming the package for the
firmware was called ``wifidriver-firmware``, you would use the
following in the ``.conf`` file for the machine::

   MACHINE_EXTRA_RDEPENDS += "wifidriver-firmware"
