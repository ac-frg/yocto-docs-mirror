Directs BitBake to exclude a recipe from world builds (i.e.
``bitbake world``). During world builds, BitBake locates, parses and
builds all recipes found in every layer exposed in the
``bblayers.conf`` configuration file.

To exclude a recipe from a world build using this variable, set the
variable to "1" in the recipe.

.. note::

   Recipes added to :term:`EXCLUDE_FROM_WORLD` may still be built during a
   world build in order to satisfy dependencies of other recipes. Adding
   a recipe to :term:`EXCLUDE_FROM_WORLD` only ensures that the recipe is not
   explicitly added to the list of build targets in a world build.
