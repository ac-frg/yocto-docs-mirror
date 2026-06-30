This variable is used by the :ref:`ref-classes-kernel-fit-image` class.
The default value of :term:`FIT_KERNEL_SIGN_KEYDIR` is the value of
:term:`UBOOT_SIGN_KEYDIR`, which means the kernel is signed at build-time
with a private key found in :term:`UBOOT_SIGN_KEYDIR` and U-Boot gets the
public key from the same directory injected into its DTB for the
on-target verification of the FIT image.

If this variable is overridden, the :term:`FIT_KERNEL_SIGN_ENABLE` and
:term:`FIT_KERNEL_SIGN_KEYNAME` variables should also be set appropriately.
