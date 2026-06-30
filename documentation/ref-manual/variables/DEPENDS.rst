Lists a recipe's build-time dependencies. These are dependencies on
other recipes whose contents (e.g. headers and shared libraries) are
needed by the recipe at build time.

As an example, consider a recipe ``foo`` that contains the following
assignment::

    DEPENDS = "bar"

The practical effect of the previous assignment is that all files
installed by bar will be available in the appropriate staging sysroot,
given by the :term:`STAGING_DIR* <STAGING_DIR_HOST>` variables, by the time
the :term:`do_configure` task for ``foo`` runs. This mechanism is
implemented by having :term:`do_configure` depend on the
:term:`do_populate_sysroot` task of each recipe listed in
:term:`DEPENDS`, through a
``[``\ :ref:`deptask <bitbake-user-manual/bitbake-user-manual-metadata:variable flags>`\ ``]``
declaration in the :ref:`ref-classes-base` class.

.. note::

   It seldom is necessary to reference, for example, :term:`STAGING_DIR_HOST`
   explicitly. The standard classes and build-related variables are
   configured to automatically use the appropriate staging sysroots.

As another example, :term:`DEPENDS` can also be used to add utilities
that run on the build machine during the build. For example, a recipe
that makes use of a code generator built by the recipe ``codegen``
might have the following::

   DEPENDS = "codegen-native"

For more
information, see the :ref:`ref-classes-native` class and
the :term:`EXTRANATIVEPATH` variable.

.. note::

   -  :term:`DEPENDS` is a list of recipe names. Or, to be more precise,
      it is a list of :term:`PROVIDES` names, which
      usually match recipe names. Putting a package name such as
      "foo-dev" in :term:`DEPENDS` does not make sense. Use "foo"
      instead, as this will put files from all the packages that make
      up ``foo``, which includes those from ``foo-dev``, into the
      sysroot.

   -  One recipe having another recipe in :term:`DEPENDS` does not by
      itself add any runtime dependencies between the packages
      produced by the two recipes. However, as explained in the
      ":ref:`overview-manual/concepts:automatically added runtime dependencies`"
      section in the Yocto Project Overview and Concepts Manual,
      runtime dependencies will often be added automatically, meaning
      :term:`DEPENDS` alone is sufficient for most recipes.

   -  Counterintuitively, :term:`DEPENDS` is often necessary even for
      recipes that install precompiled components. For example, if
      ``libfoo`` is a precompiled library that links against
      ``libbar``, then linking against ``libfoo`` requires both
      ``libfoo`` and ``libbar`` to be available in the sysroot.
      Without a :term:`DEPENDS` from the recipe that installs ``libfoo``
      to the recipe that installs ``libbar``, other recipes might
      fail to link against ``libfoo``.

For information on runtime dependencies, see the :term:`RDEPENDS`
variable. You can also see the
":ref:`bitbake-user-manual/bitbake-user-manual-metadata:tasks`" and
":ref:`bitbake-user-manual/bitbake-user-manual-execution:dependencies`"
sections in the BitBake User Manual for additional information on tasks
and dependencies.
