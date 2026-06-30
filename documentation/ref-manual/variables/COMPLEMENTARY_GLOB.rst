Defines wildcards to match when installing a list of complementary
packages for all the packages explicitly (or implicitly) installed in
an image.

The :term:`COMPLEMENTARY_GLOB` variable uses Unix filename pattern matching
(`fnmatch <https://docs.python.org/3/library/fnmatch.html#module-fnmatch>`__),
which is similar to the Unix style pathname pattern expansion
(`glob <https://docs.python.org/3/library/glob.html>`__).

The resulting list of complementary packages is associated with an
item that can be added to
:term:`IMAGE_FEATURES`. An example usage of
this is the "dev-pkgs" item that when added to :term:`IMAGE_FEATURES`
will install -dev packages (containing headers and other development
files) for every package in the image.

To add a new feature item pointing to a wildcard, use a variable flag
to specify the feature item name and use the value to specify the
wildcard. Here is an example::

   COMPLEMENTARY_GLOB[dev-pkgs] = '*-dev'

.. note::

   When installing complementary packages, recommends relationships
   (set via :term:`RRECOMMENDS`) are always ignored.
