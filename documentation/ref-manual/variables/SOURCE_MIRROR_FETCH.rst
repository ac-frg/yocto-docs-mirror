When you are fetching files to create a mirror of sources (i.e.
creating a source mirror), setting :term:`SOURCE_MIRROR_FETCH` to "1" in
your ``local.conf`` configuration file ensures the source for all
recipes are fetched regardless of whether or not a recipe is
compatible with the configuration. A recipe is considered
incompatible with the currently configured machine when either or
both the :term:`COMPATIBLE_MACHINE`
variable and :term:`COMPATIBLE_HOST` variables
specify compatibility with a machine other than that of the current
machine or host.

.. note::

   Do not set the :term:`SOURCE_MIRROR_FETCH`
   variable unless you are creating a source mirror. In other words,
   do not set the variable during a normal build.
