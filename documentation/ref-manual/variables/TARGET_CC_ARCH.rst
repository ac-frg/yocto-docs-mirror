Specifies architecture-specific C compiler flags for the target
system. :term:`TARGET_CC_ARCH` is initialized from
:term:`TUNE_CCARGS` by default.

.. note::

   It is a common workaround to append :term:`LDFLAGS` to
   :term:`TARGET_CC_ARCH` in recipes that build software for the target that
   would not otherwise respect the exported :term:`LDFLAGS` variable.
