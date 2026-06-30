Specifies architecture-specific assembler flags for the target
system. The set of flags is based on the selected tune features.
:term:`TUNE_ASARGS` is set using the tune include files, which are
typically under ``meta/conf/machine/include/`` and are influenced
through :term:`TUNE_FEATURES`. For example, the
``meta/conf/machine/include/x86/arch-x86.inc`` file defines the flags
for the x86 architecture as follows::

   TUNE_ASARGS += "${@bb.utils.contains("TUNE_FEATURES", "mx32", "-x32", "", d)}"

.. note::

   Board Support Packages (BSPs) select the tune. The selected tune,
   in turn, affects the tune variables themselves (i.e. the tune can
   supply its own set of flags).
