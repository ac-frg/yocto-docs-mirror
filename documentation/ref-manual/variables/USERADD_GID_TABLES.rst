Specifies a password file to use for obtaining static group
identification (``gid``) values when the OpenEmbedded build system
adds a group to the system during package installation.

When applying static group identification (``gid``) values, the
OpenEmbedded build system looks in :term:`BBPATH` for a
``files/group`` file and then applies those ``uid`` values. Set the
variable as follows in your ``local.conf`` file::


   USERADD_GID_TABLES = "files/group"

.. note::

   Setting the :term:`USERADDEXTENSION` variable to "useradd-staticids"
   causes the build system to use static ``gid`` values.
