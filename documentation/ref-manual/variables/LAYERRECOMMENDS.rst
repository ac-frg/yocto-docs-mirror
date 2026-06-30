Lists the layers, separated by spaces, recommended for use with this
layer.

Optionally, you can specify a specific layer version for a
recommendation by adding the version to the end of the layer name.
Here is an example::

   LAYERRECOMMENDS_mylayer = "anotherlayer (=3)"

In this previous example, version 3 of "anotherlayer" is compared
against ``LAYERVERSION_anotherlayer``.

This variable is used in the ``conf/layer.conf`` file and must be
suffixed with the name of the specific layer (e.g.
``LAYERRECOMMENDS_mylayer``).
