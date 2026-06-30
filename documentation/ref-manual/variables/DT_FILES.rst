Space-separated list of device tree source files to compile using
a recipe that inherits the :ref:`ref-classes-devicetree` class. These
are relative to the :term:`DT_FILES_PATH`.

For convenience, both ``.dts`` and ``.dtb`` extensions can be used.

Use an empty string (default) to build all device tree sources within
the :term:`DT_FILES_PATH` directory.
