If the :term:`IMAGE_FSTYPES` variable contains "wic", the build
will generate a
:ref:`Wic image <dev-manual/wic:creating partitioned images using wic>`
automatically when BitBake builds an image recipe. As part of
this process BitBake will invoke the "`wic create`" command. The
:term:`WIC_CREATE_EXTRA_ARGS` variable is placed at the end of this
command which allows the user to supply additional arguments.

One such useful purpose for this mechanism is to add the ``-D`` (or
``--debug``) argument to the "`wic create`" command. This increases the
amount of debugging information written out to the Wic log during the
Wic creation process.
