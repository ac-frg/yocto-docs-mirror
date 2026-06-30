Lists the layers to enable during the build. This variable is defined
in the ``bblayers.conf`` configuration file in the :term:`Build Directory`.
Here is an example::

   BBLAYERS = " \
       /home/scottrif/bitbake-builds/layers/meta \
       /home/scottrif/bitbake-builds/layers/meta-poky \
       /home/scottrif/bitbake-builds/layers/meta-yocto-bsp \
       /home/scottrif/bitbake-builds/layers/meta-mykernel \
       "

This example enables four layers, one of which is a custom,
user-defined layer named ``meta-mykernel``.
