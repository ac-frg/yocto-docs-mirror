The maximum number of tasks BitBake should run in parallel at any one
time. The OpenEmbedded build system automatically configures this
variable to be equal to the number of cores on the build system. For
example, a system with a dual core processor that also uses
hyper-threading causes the :term:`BB_NUMBER_THREADS` variable to default
to "4".

For single socket systems (i.e. one CPU), you should not have to
override this variable to gain optimal parallelism during builds.
However, if you have very large systems that employ multiple physical
CPUs, you might want to make sure the :term:`BB_NUMBER_THREADS` variable
is not set higher than "20".

For more information on speeding up builds, see the
":ref:`dev-manual/speeding-up-build:speeding up a build`"
section in the Yocto Project Development Tasks Manual.

On the other hand, if your goal is to limit the amount of system
resources consumed by BitBake tasks, setting :term:`BB_NUMBER_THREADS`
to a number lower than the number of CPU threads in your machine
won't be sufficient. That's because each package will still be built
and installed through a number of parallel jobs specified by the
:term:`PARALLEL_MAKE` variable, which is by default the number of CPU
threads in your system, and is not impacted by the
:term:`BB_NUMBER_THREADS` value.

So, if you set :term:`BB_NUMBER_THREADS` to "1" but don't set
:term:`PARALLEL_MAKE`, most of your system resources will be consumed
anyway.

Therefore, if you intend to reduce the load of your build system by
setting :term:`BB_NUMBER_THREADS` to a relatively low value compared
to the number of CPU threads on your system, you should also set
:term:`PARALLEL_MAKE` to a similarly low value.

An alternative to using :term:`BB_NUMBER_THREADS` to keep the usage
of build system resources under control is to use the smarter
:term:`BB_PRESSURE_MAX_CPU`, :term:`BB_PRESSURE_MAX_IO` or
:term:`BB_PRESSURE_MAX_MEMORY` controls. See the
:doc:`/dev-manual/limiting-resources` section of the Yocto Project
Development Tasks Manual.
