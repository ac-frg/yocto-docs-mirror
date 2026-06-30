The pathname of the work directory in which the OpenEmbedded build
system builds a recipe. This directory is located within the
:term:`TMPDIR` directory structure and is specific to
the recipe being built and the system for which it is being built.

The :term:`WORKDIR` directory is defined as follows::

   ${TMPDIR}/work/${MULTIMACH_TARGET_SYS}/${PN}/${EXTENDPE}${PV}-${PR}

The actual directory depends on several things:

-  :term:`TMPDIR`: The top-level build output directory
-  :term:`MULTIMACH_TARGET_SYS`: The target system identifier
-  :term:`PN`: The recipe name
-  :term:`EXTENDPE`: The epoch --- if :term:`PE` is not specified, which
   is usually the case for most recipes, then :term:`EXTENDPE` is blank.
-  :term:`PV`: The recipe version
-  :term:`PR`: The recipe revision

As an example, assume a Source Directory top-level folder name
``bitbake-builds``, a default :term:`Build Directory` at ``bitbake-builds/build``, and a
``qemux86-poky-linux`` machine target system. Furthermore, suppose
your recipe is named ``foo_1.3.0-r0.bb``. In this case, the work
directory the build system uses to build the package would be as
follows::

   bitbake-builds/build/tmp/work/qemux86-poky-linux/foo/1.3.0-r0
