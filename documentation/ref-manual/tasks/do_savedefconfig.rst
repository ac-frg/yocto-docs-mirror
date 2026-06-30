When invoked by the user, creates a defconfig file that can be used
instead of the default defconfig. The saved defconfig contains the
differences between the default defconfig and the changes made by the
user using other methods (i.e. the
:term:`do_menuconfig` task. You
can invoke the task using the following command::

   $ bitbake linux-yocto -c savedefconfig
