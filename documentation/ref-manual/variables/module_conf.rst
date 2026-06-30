Specifies `modprobe.d <https://linux.die.net/man/5/modprobe.d>`__
syntax lines for inclusion in the ``/etc/modprobe.d/modname.conf``
file.

You can use this variable anywhere that it can be recognized by the
kernel recipe or out-of-tree kernel module recipe (e.g. a machine
configuration file, a distribution configuration file, an append file
for the recipe, or the recipe itself). If you use this variable, you
must also be sure to list the module name in the
:term:`KERNEL_MODULE_PROBECONF`
variable.

Here is the general syntax::

   module_conf_module_name = "modprobe.d-syntax"

You must use the kernel module name override.

Run ``man modprobe.d`` in the shell to find out more information on
the exact syntax you want to provide with :term:`module_conf`.

Including :term:`module_conf` causes the OpenEmbedded build system to
populate the ``/etc/modprobe.d/modname.conf`` file with
``modprobe.d`` syntax lines. Here is an example that adds the options
``arg1`` and ``arg2`` to a module named ``mymodule``::

   module_conf_mymodule = "options mymodule arg1=val1 arg2=val2"

For information on how to specify kernel modules to auto-load on
boot, see the :term:`KERNEL_MODULE_AUTOLOAD` variable.
