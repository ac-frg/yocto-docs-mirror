The :term:`KERNEL_CONSOLE` variable holds the value of the ``console``
parameter of the kernel command line and can be used in places such as a
``wks`` description file for :ref:`Wic images <dev-manual/wic:creating
partitioned images using wic>`.

The default value of this variable is extracted from the first console
device and setting in :term:`SERIAL_CONSOLES`. If nothing is found in
:term:`SERIAL_CONSOLES`, the default value is set to ``ttyS0,115200``.

For more information, see the `Kernel command-line documentation
<https://www.kernel.org/doc/html/latest/admin-guide/kernel-parameters.html>`__.
