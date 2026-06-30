When using the :ref:`ref-classes-barebox` class, this variable allows you
to specify a particular binary that should be deployed and installed.

The barebox build system can build multiple barebox binaries at once.
By default, all built binaries will be deployed and installed under their
original name.

Here is an example usage of this variable::

   BAREBOX_BINARY = "barebox-boundarydevices-imx6dl-nitrogen6x-1g.img"
