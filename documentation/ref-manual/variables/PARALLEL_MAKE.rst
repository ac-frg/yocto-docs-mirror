Extra options passed to the build tool command (``make``,
``ninja`` or more specific build engines, like the Go language one)
during the :term:`do_compile` task, to specify parallel compilation
on the local build host. This variable is usually in the form "-j x",
where x represents the maximum number of parallel threads such engines
can run.

.. note::

   For software compiled by ``make``, in order for :term:`PARALLEL_MAKE`
   to be effective, ``make`` must be called with
   ``${``\ :term:`EXTRA_OEMAKE`\ ``}``. An easy
   way to ensure this is to use the ``oe_runmake`` function.

By default, the OpenEmbedded build system automatically sets this
variable to be equal to the number of cores the build system uses.

.. note::

   If the software being built experiences dependency issues during
   the :term:`do_compile` task that result in race conditions, you can clear
   the :term:`PARALLEL_MAKE` variable within the recipe as a workaround. For
   information on addressing race conditions, see the
   ":ref:`dev-manual/debugging:debugging parallel make races`"
   section in the Yocto Project Development Tasks Manual.

For single socket systems (i.e. one CPU), you should not have to
override this variable to gain optimal parallelism during builds.
However, if you have very large systems that employ multiple physical
CPUs, you might want to make sure the :term:`PARALLEL_MAKE` variable is
not set higher than "-j 20".

For more information on speeding up builds, see the
":ref:`dev-manual/speeding-up-build:speeding up a build`"
section in the Yocto Project Development Tasks Manual.

For more information on how to limit the resources used during builds, see
the :doc:`/dev-manual/limiting-resources` section of the Yocto Project
Development Tasks Manual.
