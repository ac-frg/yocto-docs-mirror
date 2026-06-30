A space-separated list (filter) of tools on the build host that
should be allowed to be called from within build tasks. Using this
filter helps reduce the possibility of host contamination. If a tool
specified in the value of :term:`HOSTTOOLS` is not found on the build
host, the OpenEmbedded build system produces an error and the build
is not started.

For additional information, see
:term:`HOSTTOOLS_NONFATAL`.
