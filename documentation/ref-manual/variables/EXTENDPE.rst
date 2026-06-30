Used with file and pathnames to create a prefix for a recipe's
version based on the recipe's :term:`PE` value. If :term:`PE`
is set and greater than zero for a recipe, :term:`EXTENDPE` becomes that
value (e.g if :term:`PE` is equal to "1" then :term:`EXTENDPE` becomes "1").
If a recipe's :term:`PE` is not set (the default) or is equal to zero,
:term:`EXTENDPE` becomes "".

See the :term:`STAMP` variable for an example.
