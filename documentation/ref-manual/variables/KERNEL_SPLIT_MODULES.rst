When inheriting the :ref:`ref-classes-kernel-module-split` class, this
variable controls whether kernel modules are split into separate packages
or bundled into a single package.

For some use cases, a monolithic kernel module package
:term:`KERNEL_PACKAGE_NAME` that contains all modules built from the
kernel sources may be preferred to speed up the installation.

By default, this variable is set to ``1``, resulting in one package per
module. Setting it to any other value will generate a single monolithic
package containing all kernel modules.

.. note::

   If :term:`KERNEL_SPLIT_MODULES` is set to 0, it is still possible to
   install all kernel modules at once by adding ``kernel-modules`` (assuming
   :term:`KERNEL_PACKAGE_NAME` is ``kernel-modules``) to :term:`IMAGE_INSTALL`.
   The way it works is that a placeholder "kernel-modules" package will be
   created and will depend on every other individual kernel module packages.
