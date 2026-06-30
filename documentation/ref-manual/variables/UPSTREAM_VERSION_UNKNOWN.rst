You can perform a per-recipe check for what the latest upstream
source code version is by calling ``devtool latest-version recipe``.
If no combination of the :term:`UPSTREAM_CHECK_URI`, :term:`UPSTREAM_CHECK_REGEX`,
:term:`UPSTREAM_CHECK_GITTAGREGEX` and :term:`UPSTREAM_CHECK_COMMITS` variables in
the recipe allows to determine what the latest upstream version is,
you can set :term:`UPSTREAM_VERSION_UNKNOWN` to ``1`` in the recipe
to acknowledge that the check cannot be performed::

   UPSTREAM_VERSION_UNKNOWN = "1"
