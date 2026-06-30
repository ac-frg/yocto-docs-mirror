If defined in the BitBake environment, :term:`BBSERVER` points to the
BitBake remote server.

Use the following format to export the variable to the BitBake
environment::

   export BBSERVER=localhost:$port

By default, :term:`BBSERVER` also appears in :term:`BB_BASEHASH_IGNORE_VARS`.
Consequently, :term:`BBSERVER` is excluded from checksum and dependency
data.
