Specifies the description string encoded into a U-Boot fitImage. The default
value is set by the :ref:`ref-classes-uboot-sign` class as follows::

   UBOOT_FIT_DESC ?= "U-Boot fitImage for ${DISTRO_NAME}/${PV}/${MACHINE}"
