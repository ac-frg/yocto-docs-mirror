When used with the :ref:`ref-classes-kernel-yocto`
class, specifies an "in-tree" kernel configuration file for use
during a kernel build.

Typically, when using a ``defconfig`` to configure a kernel during a
build, you place the file in your layer in the same manner as you
would place patch files and configuration fragment files (i.e.
"out-of-tree"). However, if you want to use a ``defconfig`` file that
is part of the kernel tree (i.e. "in-tree"), you can use the
:term:`KBUILD_DEFCONFIG` variable to point to the
``defconfig`` file.

To use the variable, set it in the append file for your kernel recipe
using the following form::

   KBUILD_DEFCONFIG:<machine> ?= "defconfig_file"

Here is an example from a "raspberrypi2" :term:`MACHINE` build that uses
a ``defconfig`` file named "bcm2709_defconfig"::

   KBUILD_DEFCONFIG:raspberrypi2 = "bcm2709_defconfig"

As an alternative, you can use the following within your append file::

   KBUILD_DEFCONFIG:pn-linux-yocto ?= "defconfig_file"

For more
information on how to use the :term:`KBUILD_DEFCONFIG` variable, see the
":ref:`kernel-dev/common:using an "in-tree" \`\`defconfig\`\` file`"
section in the Yocto Project Linux Kernel Development Manual.
