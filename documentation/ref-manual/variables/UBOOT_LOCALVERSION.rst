Appends a string to the name of the local version of the U-Boot
image. For example, assuming the version of the U-Boot image built
was "2013.10", the full version string reported by U-Boot would be
"2013.10-yocto" given the following statement::

   UBOOT_LOCALVERSION = "-yocto"
