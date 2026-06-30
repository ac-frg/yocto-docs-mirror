A Trusted Execution Environment (TEE) is a secure environment for
executing code, ensuring high levels of trust in asset management within
the surrounding system. This variable enables the generation of a U-Boot
FIT image with a Trusted Execution Environment (TEE) binary.

Its default value is "0", so set it to "1" to enable this functionality::

   UBOOT_FIT_TEE = "1"
