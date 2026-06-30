Specifies the path to the Trusted Firmware-A (TF-A) binary. Its default
value is "bl31.bin"::

   UBOOT_FIT_ARM_TRUSTED_FIRMWARE_IMAGE ?= "bl31.bin"

If a relative path is provided, the file is expected to be relative to
U-Boot's :term:`B` directory. An absolute path can be provided too,
e.g.::

   UBOOT_FIT_ARM_TRUSTED_FIRMWARE_IMAGE ?= "${DEPLOY_DIR_IMAGE}/bl31.bin"

If the Trusted Firmware-A (TF-A) binary is built in a separate recipe,
you must add the necessary dependency in a U-Boot ``.bbappend`` file. The
recipe name for Trusted Firmware-A (TF-A) binary is
``trusted-firmware-a``, which comes from the
:yocto_git:`meta-arm </meta-arm>` layer::

   do_compile[depends] += "trusted-firmware-a:do_deploy"
