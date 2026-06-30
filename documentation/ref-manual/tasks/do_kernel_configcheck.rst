Validates the configuration produced by the
:term:`do_menuconfig` task. The
:term:`do_kernel_configcheck` task produces warnings when a requested
configuration does not appear in the final ``.config`` file or when you
override a policy configuration in a hardware configuration fragment.
You can run this task explicitly and view the output by using the
following command::

   $ bitbake linux-yocto -c kernel_configcheck -f

For more information, see the
":ref:`kernel-dev/common:validating configuration`"
section in the Yocto Project Linux Kernel Development Manual.
