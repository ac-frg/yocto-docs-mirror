Defines your own :term:`PREMIRRORS` from which to
first fetch source before attempting to fetch from the upstream
specified in :term:`SRC_URI`.

To use this variable, you must globally inherit the
:ref:`ref-classes-own-mirrors` class and then provide
the URL to your mirrors. Here is the general syntax::

   INHERIT += "own-mirrors"
   SOURCE_MIRROR_URL = "http://example.com/my_source_mirror"

.. note::

   You can specify only a single URL in :term:`SOURCE_MIRROR_URL`.

.. note::

   If the mirror is protected behind a username and password, the
   :term:`build host` needs to be configured so the :term:`build system
   <OpenEmbedded Build System>` is able to fetch from the mirror.

   The recommended way to do that is by setting the following parameters
   in ``$HOME/.netrc`` (``$HOME`` being the :term:`build host` home
   directory)::

      machine example.com
      login <user>
      password <password>

   This file requires permissions set to ``400`` or ``600`` to prevent
   other users from reading the file::

      chmod 600 "$HOME/.netrc"

   Another method to configure the username and password is from the URL
   in :term:`SOURCE_MIRROR_URL` directly, with the ``user`` and ``pswd``
   parameters::

      SOURCE_MIRROR_URL = "http://example.com/my_source_mirror;user=<user>;pswd=<password>"
