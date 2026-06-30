Used for constructing directory trees used during staging.

For information on how staging for recipe-specific sysroots occurs,
see the :term:`do_populate_sysroot`
task, the ":ref:`dev-manual/devtool:sharing files between recipes`"
section in the Yocto Project Development Tasks Manual, the
":ref:`overview-manual/concepts:configuration, compilation, and staging`"
section in the Yocto Project Overview and Concepts Manual, and the
:term:`SYSROOT_DIRS` variable.

.. note::

   Recipes should never write files directly under the :term:`STAGING_DIR`
   directory because the OpenEmbedded build system manages the
   directory automatically. Instead, files should be installed to
   ``${``\ :term:`D`\ ``}`` within your recipe's :term:`do_install`
   task and then the OpenEmbedded build system will stage a subset of
   those files into the sysroot.
