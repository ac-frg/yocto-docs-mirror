A list of recipes that are completely stable and will never change.
The ABI for the recipes in the list are presented by output from the
tasks run to build the recipe. Use of this variable is one way to
remove dependencies from one recipe on another that affect task
signatures and thus force rebuilds when the recipe changes.

.. note::

   If you add an inappropriate variable to this list, the software
   might break at runtime if the interface of the recipe was changed
   after the other had been built.
