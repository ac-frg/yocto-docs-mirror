You can perform a per-recipe check for what the latest upstream
source code version is by calling ``devtool latest-version recipe``. If
the source code is provided from tarballs, the latest version is
determined by fetching the directory listing where the tarball is and
attempting to find a later tarball. When this approach does not work,
you can use :term:`UPSTREAM_CHECK_URI` to provide a different URI that
contains the link to the latest tarball::

   UPSTREAM_CHECK_URI = "recipe_url"
