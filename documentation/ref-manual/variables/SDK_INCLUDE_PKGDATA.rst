When set to "1", specifies to include the packagedata for all recipes
in the "world" target in the extensible SDK. Including this data
allows the ``devtool search`` command to find these recipes in search
results, as well as allows the ``devtool add`` command to map
dependencies more effectively.

.. note::

   Enabling the :term:`SDK_INCLUDE_PKGDATA`
   variable significantly increases build time because all of world
   needs to be built. Enabling the variable also slightly increases
   the size of the extensible SDK.
