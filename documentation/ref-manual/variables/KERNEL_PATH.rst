The location of the kernel sources. This variable is set to the value
of the :term:`STAGING_KERNEL_DIR` within the :ref:`ref-classes-module`
class. For information on how this variable is used, see the
":ref:`kernel-dev/common:incorporating out-of-tree modules`"
section in the Yocto Project Linux Kernel Development Manual.

To help maximize compatibility with out-of-tree drivers used to build
modules, the OpenEmbedded build system also recognizes and uses the
:term:`KERNEL_SRC` variable, which is identical to
the :term:`KERNEL_PATH` variable. Both variables are common variables
used by external Makefiles to point to the kernel source directory.
