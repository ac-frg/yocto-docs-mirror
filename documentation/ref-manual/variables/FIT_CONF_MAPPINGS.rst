When inheriting the :ref:`ref-classes-kernel-fit-image`, the
:term:`FIT_CONF_MAPPINGS` variable allows specifying mappings to rename
configuration nodes or add extra configuration nodes for existing device
tree blobs (DTBs) in FIT images. This provides flexibility when a 1 to 1
mapping between DTB names and configuration node names does not work,
such as when the kernel defines a kernel specific name but the bootloader
uses a different name. This might be the case when maintaining
compatibility with existing boot scripts or bootloader configurations.
But there are other use cases as well.

The variable accepts a space-separated list of mapping commands:

-  ``dtb-conf:DTB_NAME:NEW_NAME``
   Renames the configuration node for a specific DTB. The ``DTB_NAME`` is
   the name of the DTB without its ``.dtb`` suffix.

-  ``dtb-extra-conf:DTB_NAME:EXTRA_NAME``
   Creates an additional configuration node for an existing DTB. This is
   useful when you need to provide alternative names for the same hardware
   configuration to maintain compatibility with existing boot scripts or
   bootloader configurations or just need an alias configuration name for
   some other reason.

For example::

   FIT_CONF_MAPPINGS = "\
       dtb-extra-conf:am335x-bonegreen:bonegreen \
       dtb-conf:am335x-boneblack:bbblack"

This generates three configuration nodes from two DTBs:

-  ``am335x-bonegreen``: the original configuration node for the
   ``am335x-bonegreen`` device tree
-  ``bonegreen``: an extra configuration node for the same
   ``am335x-bonegreen`` DTB
-  ``bbblack``: a renamed configuration node for the ``am335x-boneblack`` DTB

The :ref:`ref-classes-kernel-fit-image` class validates all mappings
and ensures they match existing DTBs.
