When inheriting the :ref:`ref-classes-binconfig` class,
this variable specifies additional arguments passed to the "sed"
command. The sed command alters any paths in configuration scripts
that have been set up during compilation. Inheriting this class
results in all paths in these scripts being changed to point into the
``sysroots/`` directory so that all builds that use the script will
use the correct directories for the cross compiling layout.

See the ``meta/classes-recipe/binconfig.bbclass`` in
:term:`OpenEmbedded-Core (OE-Core)` for details on how this class
applies these additional sed command arguments.
