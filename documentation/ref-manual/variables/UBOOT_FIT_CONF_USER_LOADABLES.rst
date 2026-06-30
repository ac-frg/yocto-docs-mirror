Adds one or more user-defined images to the ``loadables`` property of the
configuration node of the U-Boot Image Tree Source (ITS). This variable
is handled by the local shell in the recipe so appropriate escaping
should be done, e.g. escaping quotes.::

   UBOOT_FIT_CONF_USER_LOADABLES = '\"fwa\", \"fwb\"'
