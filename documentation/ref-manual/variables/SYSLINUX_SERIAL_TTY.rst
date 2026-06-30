Specifies the alternate console=tty... kernel boot argument. The
variable's default value is set in the :ref:`ref-classes-syslinux`
class as follows::

   SYSLINUX_SERIAL_TTY ?= "console=ttyS0,115200"

The class checks for and uses the variable as needed.
