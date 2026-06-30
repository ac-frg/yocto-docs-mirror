Decides whether to generate the keys for signing the U-Boot fitImage if
they don't already exist. The keys are created in :term:`SPL_SIGN_KEYDIR`.
The default value is "0".

Enable this as follows::

   UBOOT_FIT_GENERATE_KEYS = "1"

This variable is used in the :ref:`ref-classes-uboot-sign` class.
