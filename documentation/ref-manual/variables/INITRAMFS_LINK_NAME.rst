The link name of the initial RAM filesystem image. This variable is
set in the ``meta/classes-recipe/kernel-artifact-names.bbclass`` file as
follows::

   INITRAMFS_LINK_NAME ?= "initramfs-${KERNEL_ARTIFACT_LINK_NAME}"

The value of the
``KERNEL_ARTIFACT_LINK_NAME`` variable, which is set in the same
file, has the following value::

   KERNEL_ARTIFACT_LINK_NAME ?= "${MACHINE}"

See the :term:`MACHINE` variable for additional
information.
