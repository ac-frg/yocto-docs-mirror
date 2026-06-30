Compiles the source code. This task runs with the current working
directory set to ``${``\ :term:`B`\ ``}``.

The default behavior of this task is to run the ``oe_runmake`` function
if a makefile (``Makefile``, ``makefile``, or ``GNUmakefile``) is found.
If no such file is found, the :term:`do_compile` task does nothing.
