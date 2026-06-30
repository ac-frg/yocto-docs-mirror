When set to "1" in an :ref:`ref-classes-image` recipe, the
:term:`OpenEmbedded Build System` will generate a companion image that
contains the debug symbols and source code for the packages installed on
the image. The :term:`OpenEmbedded Build System` does this by adding all
the available ``-dbg`` and ``-src`` packages available in the package
feed, which are automatically generated during
:ref:`overview-manual/concepts:Package Splitting`.
