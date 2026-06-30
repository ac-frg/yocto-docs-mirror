Lists the layers, separated by spaces, on which this layer depends.
Optionally, you can specify a specific layer version for a dependency
by adding it to the end of the layer name. Here is an example::

   LAYERDEPENDS_mylayer = "anotherlayer (=3)"

In this previous example,
version 3 of "anotherlayer" is compared against
:term:`LAYERVERSION`\ ``_anotherlayer``.

An error is produced if any dependency is missing or the version
numbers (if specified) do not match exactly. This variable is used in
the ``conf/layer.conf`` file and must be suffixed with the name of
the specific layer (e.g. ``LAYERDEPENDS_mylayer``).
