This variable is the base directory the OpenEmbedded build system
uses for all build output and intermediate files (other than the
shared state cache). By default, the :term:`TMPDIR` variable points to
``tmp`` within the :term:`Build Directory`.

If you want to establish this directory in a location other than the
default, you can set it to another value in your
:ref:`structure-build-conf-site.conf` configuration file::

   TMPDIR = "/another/location"

An example use for this scenario is to set :term:`TMPDIR` to a local disk,
which does not use NFS, while having the :term:`Build Directory` use NFS.

The filesystem used by :term:`TMPDIR` must have standard filesystem
semantics (i.e. mixed-case files are unique, POSIX file locking, and
persistent inodes). Due to various issues with NFS and bugs in some
implementations, NFS does not meet this minimum requirement.
Consequently, :term:`TMPDIR` cannot be on NFS.
