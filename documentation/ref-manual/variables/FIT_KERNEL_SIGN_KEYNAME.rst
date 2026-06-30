This variable is used by the :ref:`ref-classes-kernel-fit-image` class.
The default value of :term:`FIT_KERNEL_SIGN_KEYNAME` is the value of
:term:`UBOOT_SIGN_KEYNAME`, which means the kernel is signed at
build-time with a private key named according to
:term:`UBOOT_SIGN_KEYNAME` and U-Boot gets the public key with
the same name injected into its DTB for on-target verification
of the FIT image.

If this variable is overridden, the :term:`FIT_KERNEL_SIGN_ENABLE` and
:term:`FIT_KERNEL_SIGN_KEYDIR` variables should also be set appropriately.
