This variable allows to append a string to the version
of the kernel image. This corresponds to the ``CONFIG_LOCALVERSION``
kernel configuration parameter.

Using this variable is only useful when you are using a kernel recipe
inheriting the :ref:`ref-classes-kernel` class, and which doesn't
already set a local version. Therefore, setting this variable has no
impact on ``linux-yocto`` kernels.
