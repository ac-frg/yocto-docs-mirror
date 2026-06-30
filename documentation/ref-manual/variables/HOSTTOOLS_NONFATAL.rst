A space-separated list (filter) of tools on the build host that
should be allowed to be called from within build tasks. Using this
filter helps reduce the possibility of host contamination. Unlike
:term:`HOSTTOOLS`, the OpenEmbedded build system
does not produce an error if a tool specified in the value of
:term:`HOSTTOOLS_NONFATAL` is not found on the build host. Thus, you can
use :term:`HOSTTOOLS_NONFATAL` to filter optional host tools.
