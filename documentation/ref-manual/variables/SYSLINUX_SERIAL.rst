Specifies the alternate serial port or turns it off. To turn off
serial, set this variable to an empty string in your recipe. The
variable's default value is set in the
:ref:`ref-classes-syslinux` class as follows::

   SYSLINUX_SERIAL ?= "0 115200"

The class checks for and uses the variable as needed.
