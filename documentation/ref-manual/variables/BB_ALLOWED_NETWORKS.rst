Specifies a space-delimited list of hosts that the fetcher is allowed
to use to obtain the required source code. Here are
considerations surrounding this variable:

-  This host list is only used if :term:`BB_NO_NETWORK` is either not set
   or set to "0".

-  There is limited support for wildcard matching against the beginning of
   host names. For example, the following setting matches
   ``git.gnu.org``, ``ftp.gnu.org``, and ``foo.git.gnu.org``::

      BB_ALLOWED_NETWORKS = "*.gnu.org"

   .. note::

      The use of the "``*``" character only works at the beginning of
      a host name and it must be isolated from the remainder of the
      host name. You cannot use the wildcard character in any other
      location of the name or combined with the front part of the
      name.

      For example, ``*.foo.bar`` is supported, while ``*aa.foo.bar``
      is not.

-  Mirrors not in the host list are skipped and logged in debug.

-  Attempts to access networks not in the host list cause a failure.

Using :term:`BB_ALLOWED_NETWORKS` in conjunction with
:term:`PREMIRRORS` is very useful. Adding the host
you want to use to :term:`PREMIRRORS` results in the source code being
fetched from an allowed location and avoids raising an error when a
host that is not allowed is in a :term:`SRC_URI`
statement. This is because the fetcher does not attempt to use the
host listed in :term:`SRC_URI` after a successful fetch from the
:term:`PREMIRRORS` occurs.
