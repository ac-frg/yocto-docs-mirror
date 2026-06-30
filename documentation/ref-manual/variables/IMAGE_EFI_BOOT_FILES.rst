A space-separated list of files installed into the boot partition
when preparing an image using the Wic tool with the
``bootimg_efi`` source plugin. By default,
the files are
installed under the same name as the source files. To change the
installed name, separate it from the original name with a semi-colon
(;). Source files need to be located in
:term:`DEPLOY_DIR_IMAGE`. Here are two
examples::

   IMAGE_EFI_BOOT_FILES = "${KERNEL_IMAGETYPE};bz2"
   IMAGE_EFI_BOOT_FILES = "${KERNEL_IMAGETYPE} microcode.cpio"

Alternatively, source files can be picked up using a glob pattern. In
this case, the destination file must have the same name as the base
name of the source file path. To install files into a directory
within the target location, pass its name after a semi-colon (;).
Here are two examples::

   IMAGE_EFI_BOOT_FILES = "boot/loader/*"
   IMAGE_EFI_BOOT_FILES = "boot/loader/*;boot/"

The first example
installs all files from ``${DEPLOY_DIR_IMAGE}/boot/loader/``
into the root of the target partition. The second example installs
the same files into a ``boot`` directory within the target partition.

You can find information on how to use the Wic tool in the
":ref:`dev-manual/wic:creating partitioned images using wic`"
section of the Yocto Project Development Tasks Manual. Reference
material for Wic is located in the
":doc:`/ref-manual/kickstart`" chapter.
