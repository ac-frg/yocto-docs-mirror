Specifies the kernel boot default console. If you want to use a
console other than the default, set this variable in your recipe as
follows where "X" is the console number you want to use::

   SYSLINUX_DEFAULT_CONSOLE = "console=ttyX"

The :ref:`ref-classes-syslinux` class initially sets
this variable to null but then checks for a value later.
