When set, the :term:`EXTERNAL_KERNEL_TOOLS` variable indicates that these
tools are not in the source tree.

When kernel tools are available in the tree, they are preferred over
any externally installed tools. Setting the :term:`EXTERNAL_KERNEL_TOOLS`
variable tells the OpenEmbedded build system to prefer the installed
external tools. See the :ref:`ref-classes-kernel-yocto` class in
``meta/classes-recipe`` to see how the variable is used.
