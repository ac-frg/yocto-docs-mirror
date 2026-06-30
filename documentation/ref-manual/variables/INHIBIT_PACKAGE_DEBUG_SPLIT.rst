Prevents the OpenEmbedded build system from splitting out debug
information during packaging. By default, the build system splits out
debugging information during the
:term:`do_package` task. For more information on
how debug information is split out, see the
:term:`PACKAGE_DEBUG_SPLIT_STYLE`
variable.

To prevent the build system from splitting out debug information
during packaging, set the :term:`INHIBIT_PACKAGE_DEBUG_SPLIT` variable as
follows::

   INHIBIT_PACKAGE_DEBUG_SPLIT = "1"
