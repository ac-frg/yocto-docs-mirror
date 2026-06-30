This variable has been replaced by the :term:`KERNEL_MODULE_AUTOLOAD`
variable. You should replace all occurrences of :term:`module_autoload`
with additions to :term:`KERNEL_MODULE_AUTOLOAD`, for example::

   module_autoload_rfcomm = "rfcomm"

should now be replaced with::

   KERNEL_MODULE_AUTOLOAD += "rfcomm"

See the :term:`KERNEL_MODULE_AUTOLOAD` variable for more information.
