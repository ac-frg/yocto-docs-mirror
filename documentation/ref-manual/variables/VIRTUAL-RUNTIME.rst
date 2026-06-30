:term:`VIRTUAL-RUNTIME` is a commonly used prefix for defining virtual
packages for runtime usage, typically for use in :term:`RDEPENDS`
or in image definitions.

An example is ``VIRTUAL-RUNTIME_base-utils`` that makes it possible
to either use BusyBox based utilities::

   VIRTUAL-RUNTIME_base-utils = "busybox"

or their full featured implementations from GNU Coreutils
and other projects::

   VIRTUAL-RUNTIME_base-utils = "packagegroup-core-base-utils"

Here are two examples using this virtual runtime package. The
first one is in :oe_git:`initramfs-framework_1.0.bb
</openembedded-core/tree/meta/recipes-core/initrdscripts/initramfs-framework_1.0.bb>`::

   RDEPENDS:${PN} += "${VIRTUAL-RUNTIME_base-utils}"

The second example is in the :oe_git:`core-image-initramfs-boot
</openembedded-core/tree/meta/recipes-core/images/core-image-initramfs-boot.bb>`
image definition::

   PACKAGE_INSTALL = "${INITRAMFS_SCRIPTS} ${VIRTUAL-RUNTIME_base-utils} base-passwd"
