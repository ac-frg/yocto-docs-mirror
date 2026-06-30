Specifies the path to the Trusted Execution Environment (TEE) binary. Its
default value is "tee-raw.bin"::

   UBOOT_FIT_TEE_IMAGE ?= "tee-raw.bin"

If a relative path is provided, the file is expected to be relative to
U-Boot's :term:`B` directory. An absolute path can be provided too,
e.g.::

   UBOOT_FIT_TEE_IMAGE ?= "${DEPLOY_DIR_IMAGE}/tee-raw.bin"

If the Trusted Execution Environment (TEE) binary is built in a separate
recipe, you must add the necessary dependency in a U-Boot ``.bbappend``
file. The recipe name for Trusted Execution Environment (TEE) binary is
``optee-os``, which comes from the :yocto_git:`meta-arm </meta-arm>`
layer::

   do_compile[depends] += "optee-os:do_deploy"
