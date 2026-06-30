Adds one image to the ``firmware`` property of the configuration node of
the U-Boot Image Tree Source (ITS). Sets the ``firmware`` property to
select the image to boot first::

   UBOOT_FIT_CONF_FIRMWARE = "fwa"

If not set, the first entry in "loadables" is used to boot instead.
