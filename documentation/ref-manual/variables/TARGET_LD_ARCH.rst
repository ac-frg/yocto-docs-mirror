Specifies architecture-specific linker flags for the target system.
:term:`TARGET_LD_ARCH` is initialized from
:term:`TUNE_LDARGS` by default in the BitBake
configuration file (``meta/conf/bitbake.conf``)::

   TARGET_LD_ARCH = "${TUNE_LDARGS}"
