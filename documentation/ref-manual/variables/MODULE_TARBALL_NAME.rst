The base name of the kernel module tarball. This variable is set in
the ``meta/classes-recipe/kernel-artifact-names.bbclass`` file as follows::

   MODULE_TARBALL_NAME ?= "${KERNEL_ARTIFACT_NAME}"

See :term:`KERNEL_ARTIFACT_NAME` for additional information.
