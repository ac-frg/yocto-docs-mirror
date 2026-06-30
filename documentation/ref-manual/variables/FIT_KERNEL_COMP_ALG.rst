The compression algorithm to use for the kernel image inside the FIT Image.
At present, the only supported values are "gzip" (default), "lzo" or "none".
If you set this variable to anything other than "none" you may also need
to set :term:`FIT_KERNEL_COMP_ALG_EXTENSION`.

This variable is used in the :ref:`ref-classes-kernel-uboot` class.
