The revision of the source code used to build the package. This
variable applies to Subversion, Git, and Mercurial only. Note
that if you want to build a fixed revision and you want to avoid
performing a query on the remote repository every time BitBake parses
your recipe, you should specify a :term:`SRCREV` that is a full revision
identifier (e.g. the full SHA hash in git) and not just a tag.

.. note::

   For information on limitations when inheriting the latest revision
   of software using :term:`SRCREV`, see the :term:`AUTOREV` variable
   description and the
   ":ref:`dev-manual/packages:automatically incrementing a package version number`"
   section, which is in the Yocto Project Development Tasks Manual.
