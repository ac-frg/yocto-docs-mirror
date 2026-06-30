The file type for the Secondary Program Loader (SPL). Some devices
use an SPL from which to boot (e.g. the BeagleBone development
board). For such cases, you can declare the file type of the SPL
binary in the ``u-boot.inc`` include file, which is used in the
U-Boot recipe.

The SPL file type is set to "null" by default in the ``u-boot.inc``
file as follows::

   # Some versions of u-boot build an SPL (Second Program Loader) image that
   # should be packaged along with the u-boot binary as well as placed in the
   # deploy directory. For those versions they can set the following variables
   # to allow packaging the SPL.
   SPL_BINARY ?= ""
   SPL_BINARYNAME ?= "${@os.path.basename(d.getVar("SPL_BINARY"))}"
   SPL_IMAGE ?= "${SPL_BINARYNAME}-${MACHINE}-${PV}-${PR}"
   SPL_SYMLINK ?= "${SPL_BINARYNAME}-${MACHINE}"

The :term:`SPL_BINARY` variable helps form
various ``SPL_*`` variables used by the OpenEmbedded build system.

See the BeagleBone machine configuration example in the
":ref:`dev-manual/layers:adding a layer using the \`\`bitbake-layers\`\` script`"
section in the Yocto Project Board Support Package Developer's Guide
for additional information.
