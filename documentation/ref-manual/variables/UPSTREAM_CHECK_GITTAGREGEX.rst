You can perform a per-recipe check for what the latest upstream
source code version is by calling ``devtool latest-version recipe``. If
the recipe source code is provided from Git repositories, the
OpenEmbedded build system determines the latest upstream version by
picking the latest tag from the list of all repository tags.

You can use the :term:`UPSTREAM_CHECK_GITTAGREGEX` variable to provide a
regular expression to filter only the relevant tags should the
default filter not work correctly::

   UPSTREAM_CHECK_GITTAGREGEX = "git_tag_regex"
