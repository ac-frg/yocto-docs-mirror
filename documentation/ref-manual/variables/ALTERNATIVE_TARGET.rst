Used by the alternatives system to create default link locations for
duplicated commands. You can use the variable to create a single
default location for all duplicated commands regardless of the
command name or package, a default for specific duplicated commands
regardless of the package, or a default for specific commands tied to
particular packages. Here are the available syntax forms::

   ALTERNATIVE_TARGET = "target"
   ALTERNATIVE_TARGET[name] = "target"
   ALTERNATIVE_TARGET_pkg[name] = "target"

.. note::

   If :term:`ALTERNATIVE_TARGET` is not defined, it inherits the value
   from the :term:`ALTERNATIVE_LINK_NAME` variable.

   If :term:`ALTERNATIVE_LINK_NAME` and :term:`ALTERNATIVE_TARGET` are the
   same, the target for :term:`ALTERNATIVE_TARGET` has "``.{BPN}``"
   appended to it.

   Finally, if the file referenced has not been renamed, the
   alternatives system will rename it to avoid the need to rename
   alternative files in the :term:`do_install`
   task while retaining support for the command if necessary.

For more information on the alternatives system, see the
":ref:`ref-classes-update-alternatives`" section.
