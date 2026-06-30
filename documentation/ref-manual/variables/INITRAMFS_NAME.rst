The base name of the initial RAM filesystem image. This variable is
set in the ``meta/classes-recipe/kernel-artifact-names.bbclass`` file as
follows::

   INITRAMFS_NAME ?= "initramfs-${KERNEL_ARTIFACT_NAME}"

See :term:`KERNEL_ARTIFACT_NAME` for additional information.
