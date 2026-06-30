Lists kernel modules that need to be auto-loaded during boot.

.. note::

   This variable replaces the deprecated :term:`module_autoload`
   variable.

You can use the :term:`KERNEL_MODULE_AUTOLOAD` variable anywhere that it
can be recognized by the kernel recipe or by an out-of-tree kernel
module recipe (e.g. a machine configuration file, a distribution
configuration file, an append file for the recipe, or the recipe
itself).

Specify it as follows::

   KERNEL_MODULE_AUTOLOAD += "module_name1 module_name2 module_name3"

Including :term:`KERNEL_MODULE_AUTOLOAD` causes the OpenEmbedded build
system to populate the ``/etc/modules-load.d/modname.conf`` file with
the list of modules to be auto-loaded on boot. The modules appear
one-per-line in the file. Here is an example of the most common use
case::

   KERNEL_MODULE_AUTOLOAD += "module_name"

For information on how to populate the ``modname.conf`` file with
``modprobe.d`` syntax lines, see the :term:`KERNEL_MODULE_PROBECONF` variable.
