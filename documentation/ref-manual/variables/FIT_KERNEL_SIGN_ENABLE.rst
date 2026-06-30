This variable is used by the :ref:`ref-classes-kernel-fit-image` class
to enable or disable signing of the FIT image.
The default value of :term:`FIT_KERNEL_SIGN_ENABLE` is the value of
:term:`UBOOT_SIGN_ENABLE`, which means that when U-Boot FIT image signing
is enabled, the FIT image will also be signed at build-time and U-Boot
will verify the FIT image signature at run-time.

If this variable is set to "1", the FIT image will be signed using the
key specified by :term:`FIT_KERNEL_SIGN_KEYNAME` from the directory
:term:`FIT_KERNEL_SIGN_KEYDIR`.

If this variable is overridden, the :term:`FIT_KERNEL_SIGN_KEYDIR` and
:term:`FIT_KERNEL_SIGN_KEYNAME` variables should also be set appropriately.
