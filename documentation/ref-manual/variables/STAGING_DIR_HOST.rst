Specifies the path to the recipe's input sysroot directory, populated with files
for the system on which the component is built to run
(the system that hosts the component).
For most recipes, this sysroot is populated by their
:term:`do_populate_sysroot` task (when sharing files
between recipes). Exceptions include native recipes, for which the files from
:term:`do_populate_sysroot` task are instead copied to
:term:`STAGING_DIR_NATIVE`. Depending on the type of recipe and the build target,
:term:`STAGING_DIR_HOST` can have the following values:

-  For recipes building for the target machine, the value is
   ``"${RECIPE_SYSROOT}"``, check :term:`RECIPE_SYSROOT`.

-  For native recipes (building for the :term:`build host`), the value is empty
   given the assumption that when building for the :term:`build host`, the
   :term:`build host`'s own directories should be used.

   .. note::

      Native recipe files are not installed into host paths such
      as ``/usr``. Rather, such files are installed into
      :term:`STAGING_DIR_NATIVE`. When compiling native recipes,
      standard build environment variables such as
      :term:`CPPFLAGS` and
      :term:`CFLAGS` are set up so that both :term:`build host`'s paths
      and :term:`STAGING_DIR_NATIVE` are searched for libraries and
      headers using, for example, GCC's ``-isystem`` option.

      Thus, the emphasis is that the ``STAGING_DIR*`` variables
      should be viewed as input variables by tasks such as
      :term:`do_configure`,
      :term:`do_compile`, and
      :term:`do_install`. Having the real system root
      (the :term:`build host`'s root) play the role of :term:`STAGING_DIR_HOST`
      makes conceptual sense for native recipes, as they make use
      of the :term:`build host`'s headers and libraries.
