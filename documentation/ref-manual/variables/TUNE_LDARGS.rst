Specifies architecture-specific linker flags for the target system.
The set of flags is based on the selected tune features.
:term:`TUNE_LDARGS` is set using the tune include files, which are
typically under ``meta/conf/machine/include/`` and are influenced
through :term:`TUNE_FEATURES`. For example, the
``meta/conf/machine/include/x86/arch-x86.inc`` file defines the flags
for the x86 architecture as follows::

   TUNE_LDARGS += "${@bb.utils.contains("TUNE_FEATURES", "mx32", "-m elf32_x86_64", "", d)}"

.. note::

   Board Support Packages (BSPs) select the tune. The selected tune,
   in turn, affects the tune variables themselves (i.e. the tune can
   supply its own set of flags).
