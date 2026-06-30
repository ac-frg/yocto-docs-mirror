Enable signing of FIT image. The default value is "0".

This variable is defined and used by :ref:`ref-classes-uboot-config` class.

Additionally, it serves as the default value for the
:term:`FIT_KERNEL_SIGN_ENABLE` variable, which is
used by the :ref:`ref-classes-kernel-fit-image` class.

That means, if :term:`UBOOT_SIGN_ENABLE` is set to "1", the
:ref:`ref-classes-kernel-fit-image` class will sign the FIT image at
build-time using the specified private key, and the
:ref:`ref-classes-uboot-sign` class will inject the corresponding public
key into U-Boot's device tree. This makes U-Boot verify the
authenticity and integrity of the FIT image at boot time, providing a
secure boot workflow that helps prevent unauthorized or tampered images
from being loaded.

See `<https://docs.u-boot.org/en/v2025.10/usage/fit/signature.html>`__ for
more information on FIT signature verification in U-Boot.
