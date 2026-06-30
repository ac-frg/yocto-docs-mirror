This variable points to the directory populated with all files provided by
recipes specified in :term:`DEPENDS`. As the name indicates,
think of this variable as a custom root (``/``) for the recipe, that will be
used by the compiler in order to find headers and other files needed to complete
its job.

This variable is used to define :term:`STAGING_DIR_HOST` or :term:`STAGING_DIR_TARGET`
according to the type of the recipe and the build target.

To better understand this variable, consider the following examples:

-  For ``#include <header.h>``, ``header.h`` should be in ``"${RECIPE_SYSROOT}/usr/include"``

-  For ``-lexample``, ``libexample.so`` should be in ``"${RECIPE_SYSROOT}/lib"``
   or other library sysroot directories.

The default value is ``"${WORKDIR}/recipe-sysroot"``.
Do not modify it.
