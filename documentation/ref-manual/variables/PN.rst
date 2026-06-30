This variable can have two separate functions depending on the
context: a recipe name or a resulting package name.

:term:`PN` refers to a recipe name in the context of a file used by the
OpenEmbedded build system as input to create a package. The name is
normally extracted from the recipe file name. For example, if the
recipe is named ``expat_2.0.1.bb``, then the default value of :term:`PN`
will be "expat".

The variable refers to a package name in the context of a file
created or produced by the OpenEmbedded build system.

If applicable, the :term:`PN` variable also contains any special suffix
or prefix. For example, using ``bash`` to build packages for the
native machine, :term:`PN` is ``bash-native``. Using ``bash`` to build
packages for the target and for Multilib, :term:`PN` would be ``bash``
and ``lib64-bash``, respectively.
