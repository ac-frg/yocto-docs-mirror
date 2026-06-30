When invoked by the user, this task creates a file containing the
differences between the original config as produced by
:term:`do_kernel_configme` task and the
changes made by the user with other methods (i.e. using
(:term:`do_menuconfig`). Once the
file of differences is created, it can be used to create a config
fragment that only contains the differences. You can invoke this task
from the command line as follows::

   $ bitbake linux-yocto -c diffconfig

For more information, see the
":ref:`kernel-dev/common:creating configuration fragments`"
section in the Yocto Project Linux Kernel Development Manual.
