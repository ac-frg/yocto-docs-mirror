`Trusted Firmware-A (TF-A) <https://www.trustedfirmware.org/projects/tf-a>`__
is a reference implementation of secure world software for Arm A-Profile
architectures (Armv8-A and Armv7-A), including an Exception Level 3 (EL3)
Secure Monitor. This variable enables the generation of a U-Boot FIT
image with a Trusted Firmware-A (TF-A) binary.

Its default value is "0", so set it to "1" to enable this functionality::

   UBOOT_FIT_ARM_TRUSTED_FIRMWARE = "1"
