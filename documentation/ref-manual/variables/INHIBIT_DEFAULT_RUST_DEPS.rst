Prevents the :ref:`ref-classes-rust` class from automatically adding
its default build-time dependencies.

When a recipe inherits the :ref:`ref-classes-rust` class, several
tools such as ``rust-native`` and ``${RUSTLIB_DEP}`` (only added when cross-compiling) are added
to :term:`DEPENDS` to support the ``rust`` build process.

To prevent the build system from adding these dependencies automatically,
set the :term:`INHIBIT_DEFAULT_RUST_DEPS` variable as follows::

   INHIBIT_DEFAULT_RUST_DEPS = "1"

By default, the value of :term:`INHIBIT_DEFAULT_RUST_DEPS` is empty. Setting
it to "0" does not disable inhibition. Only the empty string will disable
inhibition.
