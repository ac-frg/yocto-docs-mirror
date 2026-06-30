Configures the source by enabling and disabling any build-time and
configuration options for the software being built. The task runs with
the current working directory set to ``${``\ :term:`B`\ ``}``.

The default behavior of this task is to run ``oe_runmake clean`` if a
makefile (``Makefile``, ``makefile``, or ``GNUmakefile``) is found and
:term:`CLEANBROKEN` is not set to "1". If no such
file is found or the :term:`CLEANBROKEN` variable is set to "1", the
:term:`do_configure` task does nothing.
