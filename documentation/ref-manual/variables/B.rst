The directory within the :term:`Build Directory` in which the
OpenEmbedded build system places generated objects during a recipe's
build process. By default, this directory is the same as the
:term:`S` directory, which is defined as::

   S = "${UNPACKDIR}/${BP}"

You can separate the (:term:`S`) directory and the directory pointed to
by the :term:`B` variable. Most Autotools-based recipes support
separating these directories. The build system defaults to using
separate directories for ``gcc`` and some kernel recipes.
