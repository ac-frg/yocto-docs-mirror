If set to ``error``, forces the OpenEmbedded build system to produce
an error if the user identification (``uid``) and group
identification (``gid``) values are not defined in any of the files
listed in :term:`USERADD_UID_TABLES` and
:term:`USERADD_GID_TABLES`. If set to
``warn``, a warning will be issued instead.

The default behavior for the build system is to dynamically apply
``uid`` and ``gid`` values. Consequently, the
:term:`USERADD_ERROR_DYNAMIC` variable is by default not set. If you plan
on using statically assigned ``gid`` and ``uid`` values, you should
set the :term:`USERADD_ERROR_DYNAMIC` variable in your ``local.conf``
file as follows::

   USERADD_ERROR_DYNAMIC = "error"

Overriding the
default behavior implies you are going to also take steps to set
static ``uid`` and ``gid`` values through use of the
:term:`USERADDEXTENSION`,
:term:`USERADD_UID_TABLES`, and
:term:`USERADD_GID_TABLES` variables.

.. note::

   There is a difference in behavior between setting
   :term:`USERADD_ERROR_DYNAMIC` to ``error`` and setting it to ``warn``.
   When it is set to ``warn``, the build system will report a warning for
   every undefined ``uid`` and ``gid`` in any recipe. But when it is set
   to ``error``, it will only report errors for recipes that are actually
   built.
   This saves you from having to add static IDs for recipes that you
   know will never be built.
