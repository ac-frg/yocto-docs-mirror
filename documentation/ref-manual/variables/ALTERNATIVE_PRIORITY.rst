Used by the alternatives system to create default priorities for
duplicated commands. You can use the variable to create a single
default regardless of the command name or package, a default for
specific duplicated commands regardless of the package, or a default
for specific commands tied to particular packages. Here are the
available syntax forms::

   ALTERNATIVE_PRIORITY = "priority"
   ALTERNATIVE_PRIORITY[name] = "priority"
   ALTERNATIVE_PRIORITY_pkg[name] = "priority"

For more information on the alternatives system, see the
":ref:`ref-classes-update-alternatives`"
section.
