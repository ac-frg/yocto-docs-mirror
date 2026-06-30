Assigns the priority for recipe files in each layer.

This variable is useful in situations where the same recipe appears
in more than one layer. Setting this variable allows you to
prioritize a layer against other layers that contain the same recipe
--- effectively letting you control the precedence for the multiple
layers. The precedence established through this variable stands
regardless of a recipe's version (:term:`PV` variable). For
example, a layer that has a recipe with a higher :term:`PV` value but for
which the :term:`BBFILE_PRIORITY` is set to have a lower precedence still
has a lower precedence.

A larger value for the :term:`BBFILE_PRIORITY` variable results in a
higher precedence. For example, the value 6 has a higher precedence
than the value 5. If not specified, the :term:`BBFILE_PRIORITY` variable
is set based on layer dependencies (see the :term:`LAYERDEPENDS` variable
for more information. The default priority, if unspecified for a
layer with no dependencies, is the lowest defined priority + 1 (or 1
if no priorities are defined).

.. tip::

   You can use the command ``bitbake-layers show-layers``
   to list all configured layers along with their priorities.
