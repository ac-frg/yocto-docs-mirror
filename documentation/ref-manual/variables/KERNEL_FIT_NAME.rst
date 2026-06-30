The base name of the kernel flattened image tree (FIT) image. This
variable is set in the ``meta/classes-recipe/kernel-artifact-names.bbclass``
file as follows::

   KERNEL_FIT_NAME ?= "${KERNEL_ARTIFACT_NAME}"

See :term:`KERNEL_ARTIFACT_NAME` for additional information.
