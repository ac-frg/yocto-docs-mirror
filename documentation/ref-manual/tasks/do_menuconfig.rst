Invoked by the user to manipulate the ``.config`` file used to build a
linux-yocto recipe. This task starts the Linux kernel configuration
tool, which you then use to modify the kernel configuration.

You can invoke this tool from the command line as follows:

.. code-block:: console

   $ bitbake linux-yocto -c menuconfig

See the ":ref:`kernel-dev/common:using ``menuconfig```"
section in the Yocto Project Linux Kernel Development Manual for more
information on this configuration tool.
