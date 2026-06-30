Path to additional licenses used during the build. By default, the
OpenEmbedded build system uses :term:`COMMON_LICENSE_DIR` to define the
directory that holds common license text used during the build. The
:term:`LICENSE_PATH` variable allows you to extend that location to other
areas that have additional licenses::

   LICENSE_PATH += "path-to-additional-common-licenses"
