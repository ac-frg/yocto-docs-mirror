Specifies architecture-specific C compiler flags for the target
system. The set of flags is based on the selected tune features.
:term:`TUNE_CCARGS` is set using the tune include files, which are
typically under ``meta/conf/machine/include/`` and are influenced
through :term:`TUNE_FEATURES`.

.. note::

   Board Support Packages (BSPs) select the tune. The selected tune,
   in turn, affects the tune variables themselves (i.e. the tune can
   supply its own set of flags).
