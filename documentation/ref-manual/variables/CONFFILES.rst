Identifies editable or configurable files that are part of a package.
If the Package Management System (PMS) is being used to update
packages on the target system, it is possible that configuration
files you have changed after the original installation and that you
now want to remain unchanged are overwritten. In other words,
editable files might exist in the package that you do not want reset
as part of the package update process. You can use the :term:`CONFFILES`
variable to list the files in the package that you wish to prevent
the PMS from overwriting during this update process.

To use the :term:`CONFFILES` variable, provide a package name override
that identifies the resulting package. Then, provide a
space-separated list of files. Here is an example::

   CONFFILES:${PN} += "${sysconfdir}/file1 \
       ${sysconfdir}/file2 ${sysconfdir}/file3"

There is a relationship between the :term:`CONFFILES` and :term:`FILES`
variables. The files listed within :term:`CONFFILES` must be a subset of
the files listed within :term:`FILES`. Because the configuration files
you provide with :term:`CONFFILES` are simply being identified so that
the PMS will not overwrite them, it makes sense that the files must
already be included as part of the package through the :term:`FILES`
variable.

.. note::

   When specifying paths as part of the :term:`CONFFILES` variable, it is
   good practice to use appropriate path variables.
   For example, ``${sysconfdir}`` rather than ``/etc`` or ``${bindir}``
   rather than ``/usr/bin``. You can find a list of these variables at
   the top of the ``meta/conf/bitbake.conf`` file in
   :term:`OpenEmbedded-Core (OE-Core)`.
