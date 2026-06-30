Space-separated list of loadables to add to a FIT image in addition to
regular ones (kernel, initramfs, dtsb etc.).
Values specified here will be used as node names inside the FIT image;
all of them will be included in all configurations by using the
``loadables`` property.

For each loadable specified in this variable, additional parameters can be
defined using :term:`FIT_LOADABLE_ARCH`, :term:`FIT_LOADABLE_COMPRESSION`,
:term:`FIT_LOADABLE_DESCRIPTION`, :term:`FIT_LOADABLE_ENTRYPOINT`,
:term:`FIT_LOADABLE_FILENAME`, :term:`FIT_LOADABLE_LOADADDRESS`,
:term:`FIT_LOADABLE_OS` and :term:`FIT_LOADABLE_TYPE`.

This variable is used by the :ref:`ref-classes-kernel-fit-image` class and
is empty by default.

For example, the following configuration adds as loadables a TF-A BL31
firmware and a (compressed) TEE firmware, to be loaded respectively at
0x204E0000 and 0x96000000::

   FIT_LOADABLES = "atf tee"

   FIT_LOADABLE_FILENAME[atf] = "bl31.bin"
   FIT_LOADABLE_DESCRIPTION[atf] = "TF-A Firmware"
   FIT_LOADABLE_TYPE[atf] = "tfa-bl31"
   FIT_LOADABLE_ARCH[atf] = "arm64"
   FIT_LOADABLE_OS[atf] = "arm-trusted-firmware"
   FIT_LOADABLE_LOADADDRESS[atf] = "0x204E0000"
   FIT_LOADABLE_ENTRYPOINT[atf] = "0x204E0000"

   FIT_LOADABLE_FILENAME[tee] = "tee.bin.gz"
   FIT_LOADABLE_COMPRESSION[tee] = "gzip"
   FIT_LOADABLE_TYPE[tee] = "tee"
   FIT_LOADABLE_OS[tee] = "tee"
   FIT_LOADABLE_LOADADDRESS[tee] = "0x96000000"

and will be converted to the following FIT source::

   images {
           atf {
                   description = "TF-A Firmware";
                   type = "tfa-bl31";
                   compression = "none";
                   data = /incbin/("<DEPLOY_DIR_IMAGE>/bl31.bin");
                   arch = "arm64";
                   os = "arm-trusted-firmware";
                   load = <0x204E0000>;
                   entry = <0x204E0000>;
           };
           tee {
                   description = "tee loadable";
                   type = "tee";
                   compression = "gzip";
                   data = /incbin/("<DEPLOY_DIR_IMAGE>/tee.bin.gz");
                   arch = "arm64";
                   os = "tee";
                   load = <0x96000000>;
           };
   };

   configurations {
           default = "<my-board>.dtb";
           <my-board>.dtb {
                   description = "1 Linux kernel, FDT blob, loadables";
                   kernel = "kernel-1";
                   fdt = "<my-board>.dtb";
                   loadables = "atf", "tee";
           };
   };
