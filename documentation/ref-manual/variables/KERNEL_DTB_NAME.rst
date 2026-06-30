The base name of the kernel device tree binary (DTB). This variable
is set in the ``meta/classes-recipe/kernel-artifact-names.bbclass`` file as
follows::

   KERNEL_DTB_NAME ?= "${KERNEL_ARTIFACT_NAME}"

See :term:`KERNEL_ARTIFACT_NAME` for additional information.
