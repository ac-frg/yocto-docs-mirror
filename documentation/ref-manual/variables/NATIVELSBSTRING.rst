A string identifying the host distribution. Strings consist of the
host distributor ID followed by the release, as reported by the
``lsb_release`` tool or as read from ``/etc/lsb-release``. For
example, when running a build on Ubuntu 12.10, the value is
"Ubuntu-12.10". If this information is unable to be determined, the
value resolves to "Unknown".

This variable is used by default to isolate native shared state
packages for different distributions (e.g. to avoid problems with
``glibc`` version incompatibilities). Additionally, the variable is
checked against
:term:`SANITY_TESTED_DISTROS` if that
variable is set.
