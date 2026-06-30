Value of the Meson ``--buildtype`` argument used by the
:ref:`ref-classes-meson` class. It defaults to ``debug`` if
:term:`DEBUG_BUILD` is set to "1", and ``plain`` otherwise.

See `Meson build options <https://mesonbuild.com/Builtin-options.html>`__
for the values you could set in a recipe. Values such as ``plain``,
``debug``, ``debugoptimized``, ``release`` and ``minsize`` allow
you to specify the inclusion of debugging symbols and the compiler
optimizations (none, performance or size).
