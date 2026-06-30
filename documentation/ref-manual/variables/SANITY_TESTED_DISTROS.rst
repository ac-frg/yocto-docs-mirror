A list of the host distribution identifiers that the build system has
been tested against. Identifiers consist of the host distributor ID
followed by the release, as reported by the ``lsb_release`` tool or
as read from ``/etc/lsb-release``. Separate the list items with
explicit newline characters (``\n``). If :term:`SANITY_TESTED_DISTROS` is
not empty and the current value of
:term:`NATIVELSBSTRING` does not appear in the
list, then the build system reports a warning that indicates the
current host distribution has not been tested as a build host.
