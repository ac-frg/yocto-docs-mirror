Specifies the name of all of the build artifacts. You can change the
name of the artifacts by changing the :term:`KERNEL_ARTIFACT_NAME`
variable.

The value of :term:`KERNEL_ARTIFACT_NAME`, which is set in the
``meta/classes-recipe/kernel-artifact-names.bbclass`` file, has the
following default value::

   KERNEL_ARTIFACT_NAME ?= "${PKGE}-${PKGV}-${PKGR}${IMAGE_MACHINE_SUFFIX}${IMAGE_VERSION_SUFFIX}"

See the :term:`PKGE`, :term:`PKGV`, :term:`PKGR`, :term:`IMAGE_MACHINE_SUFFIX`
and :term:`IMAGE_VERSION_SUFFIX` variables for additional information.
