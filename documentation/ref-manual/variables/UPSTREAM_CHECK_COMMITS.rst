You can perform a per-recipe check for what the latest upstream
source code version is by calling ``devtool latest-version recipe``. If
the recipe source code is provided from Git repositories, but
releases are not identified by Git tags, set :term:`UPSTREAM_CHECK_COMMITS`
to ``1`` in the recipe, and the OpenEmbedded build system
will compare the latest commit with the one currently specified
by the recipe (:term:`SRCREV`)::

   UPSTREAM_CHECK_COMMITS = "1"
