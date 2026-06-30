A list of machine-specific packages to install as part of the image
being built that are not essential for booting the machine. The image
being built has no build dependency on this list of packages.

This variable affects only images based on ``packagegroup-base``,
which does not include the ``core-image-minimal`` or
``core-image-full-cmdline`` images.

This variable is similar to the :term:`MACHINE_EXTRA_RDEPENDS` variable
with the exception that the image being built does not have a build
dependency on the variable's list of packages. In other words, the
image will build if a file in this list is not found.

An example is a machine that has WiFi capability but is not essential
For the machine to boot the image. However, if you are building a
more fully-featured image, you want to enable WiFi. In this case, the
package containing the WiFi kernel module will not be produced if the
WiFi driver is built into the kernel, in which case you still want
the build to succeed instead of failing as a result of the package
not being found. To accomplish this, assuming the package for the
module was called ``kernel-module-examplewifi``, you would use the
following in the ``.conf`` file for the machine::

   MACHINE_EXTRA_RRECOMMENDS += "kernel-module-examplewifi"
