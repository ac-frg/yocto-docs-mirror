If set to "1" within a recipe, :term:`CLEANBROKEN` specifies that the
``make clean`` command does not work for the software being built.
Consequently, the OpenEmbedded build system will not try to run
``make clean`` during the :term:`do_configure`
task, which is the default behavior.
