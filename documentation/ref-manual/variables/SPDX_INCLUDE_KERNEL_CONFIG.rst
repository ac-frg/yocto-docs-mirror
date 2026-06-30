This option allows exporting the Linux kernel configuration
(the contents of the ``.config`` file) into the recipe's SPDX
document as a separate ``build_Build`` object. Each kernel
configuration parameter (``CONFIG_*``) is recorded and linked to
the main kernel object using an ``ancestorOf`` relationship.

.. note::

   This variable only has effect when using the SPDX 3.0 output
   format (see :ref:`ref-classes-create-spdx`).

Enable this option as follows::

   SPDX_INCLUDE_KERNEL_CONFIG = "1"

When enabled, a separate SPDX object is created for the kernel
configuration, improving reproducibility, compliance tracking,
and auditing of build-time kernel features.
