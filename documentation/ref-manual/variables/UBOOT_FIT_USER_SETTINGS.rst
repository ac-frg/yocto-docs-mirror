Add a user-specific snippet to the U-Boot Image Tree Source (ITS). This
variable allows the user to add one or more user-defined ``/images`` node
to the U-Boot Image Tree Source (ITS). For more details, please refer to
https://fitspec.osfw.foundation/\ .

The original content of the U-Boot Image Tree Source (ITS) is as
follows::

   images {
       uboot {
           description = "U-Boot image";
           data = /incbin/("u-boot-nodtb.bin");
           type = "standalone";
           os = "u-boot";
           arch = "";
           compression = "none";
           load = <0x80000000>;
           entry = <0x80000000>;
       };
   };

Users can include their custom ITS snippet in this variable, e.g.::

   UBOOT_FIT_FWA_ITS = '\
       fwa {\n\
           description = \"FW A\";\n\
           data = /incbin/(\"fwa.bin\");\n\
           type = \"firmware\";\n\
           arch = \"\";\n\
           os = \"\";\n\
           load = <0xb2000000>;\n\
           entry = <0xb2000000>;\n\
           compression = \"none\";\n\
       };\n\
   '

   UBOOT_FIT_USER_SETTINGS = "${UBOOT_FIT_FWA_ITS}"

This variable is handled by the local shell in the recipe so appropriate
escaping should be done, e.g. escaping quotes and adding newlines with
``\n``.

The generated content of the U-Boot Image Tree Source (ITS) is as
follows::

   images {
       uboot {
           description = "U-Boot image";
           data = /incbin/("u-boot-nodtb.bin");
           type = "standalone";
           os = "u-boot";
           arch = "";
           compression = "none";
           load = <0x80000000>;
           entry = <0x80000000>;
       };
       fwa {
           description = "FW A";
           data = /incbin/("fwa.bin");
           type = "firmware";
           arch = "";
           os = "";
           load = <0xb2000000>;
           entry = <0xb2000000>;
           compression = "none";
       };
   };
