Specifies a password file to use for obtaining static user
identification (``uid``) values when the OpenEmbedded build system
adds a user to the system during package installation.

When applying static user identification (``uid``) values, the
OpenEmbedded build system looks in :term:`BBPATH` for a
``files/passwd`` file and then applies those ``uid`` values. Set the
variable as follows in your ``local.conf`` file::

   USERADD_UID_TABLES = "files/passwd"

.. note::

   Setting the :term:`USERADDEXTENSION` variable to "useradd-staticids"
   causes the build system to use static ``uid`` values.
