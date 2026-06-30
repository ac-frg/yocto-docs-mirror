A list of recommended machine-specific packages to install as part of
the image being built. The build process does not depend on these
packages being present. However, because this is a
"machine-essential" variable, the list of packages are essential for
the machine to boot. The impact of this variable affects images based
on ``packagegroup-core-boot``, including the ``core-image-minimal``
image.

This variable is similar to the :term:`MACHINE_ESSENTIAL_EXTRA_RDEPENDS`
variable with the exception that the image being built does not have
a build dependency on the variable's list of packages. In other
words, the image will still build if a package in this list is not
found. Typically, this variable is used to handle essential kernel
modules, whose functionality may be selected to be built into the
kernel rather than as a module, in which case a package will not be
produced.

Consider an example where you have a custom kernel where a specific
touchscreen driver is required for the machine to be usable. However,
the driver can be built as a module or into the kernel depending on
the kernel configuration. If the driver is built as a module, you
want it to be installed. But, when the driver is built into the
kernel, you still want the build to succeed. This variable sets up a
"recommends" relationship so that in the latter case, the build will
not fail due to the missing package. To accomplish this, assuming the
package for the module was called ``kernel-module-ab123``, you would
use the following in the machine's ``.conf`` configuration file::

   MACHINE_ESSENTIAL_EXTRA_RRECOMMENDS += "kernel-module-ab123"

.. note::

   In this example, the ``kernel-module-ab123`` recipe needs to
   explicitly set its :term:`PACKAGES` variable to ensure that BitBake
   does not use the kernel recipe's :term:`PACKAGES_DYNAMIC` variable to
   satisfy the dependency.

Some examples of these machine essentials are flash, screen,
keyboard, mouse, or touchscreen drivers (depending on the machine).
