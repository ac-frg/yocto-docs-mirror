When set to "useradd-staticids", causes the OpenEmbedded build system
to base all user and group additions on a static ``passwd`` and
``group`` files found in :term:`BBPATH`.

To use static user identification (``uid``) and group identification
(``gid``) values, set the variable as follows in your ``local.conf``
file: USERADDEXTENSION = "useradd-staticids"

.. note::

   Setting this variable to use static ``uid`` and ``gid``
   values causes the OpenEmbedded build system to employ the
   :ref:`ref-classes-useradd` class.

If you use static ``uid`` and ``gid`` information, you must also
specify the ``files/passwd`` and ``files/group`` files by setting the
:term:`USERADD_UID_TABLES` and
:term:`USERADD_GID_TABLES` variables.
Additionally, you should also set the
:term:`USERADD_ERROR_DYNAMIC` variable.
