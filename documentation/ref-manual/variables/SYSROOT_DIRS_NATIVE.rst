Extra directories staged into the sysroot by the
:term:`do_populate_sysroot` task for
``-native`` recipes, in addition to those specified in
:term:`SYSROOT_DIRS`. By default, the following
extra directories are staged::

   SYSROOT_DIRS_NATIVE = " \
       ${bindir} \
       ${sbindir} \
       ${base_bindir} \
       ${base_sbindir} \
       ${libexecdir} \
       ${sysconfdir} \
       ${localstatedir} \
       "

.. note::

   Programs built by ``-native`` recipes run directly from the sysroot
   (:term:`STAGING_DIR_NATIVE`), which is why additional directories
   containing program executables and supporting files need to be staged.
