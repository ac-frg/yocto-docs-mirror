Specifies architecture-specific assembler flags for the target
system. :term:`TARGET_AS_ARCH` is initialized from
:term:`TUNE_ASARGS` by default in the BitBake
configuration file (``meta/conf/bitbake.conf``)::

   TARGET_AS_ARCH = "${TUNE_ASARGS}"
