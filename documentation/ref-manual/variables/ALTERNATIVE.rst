Lists commands in a package that need an alternative binary naming
scheme. Sometimes the same command is provided in multiple packages.
When this occurs, the OpenEmbedded build system needs to use the
alternatives system to create a different binary naming scheme so the
commands can co-exist.

To use the variable, list out the package's commands that are also
provided by another package. For example, if the ``busybox`` package
has four such commands, you identify them as follows::

   ALTERNATIVE:busybox = "sh sed test bracket"

For more information on the alternatives system, see the
":ref:`ref-classes-update-alternatives`"
section.
