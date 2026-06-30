A list of recipe dependencies that should not be used to determine
signatures of tasks from one recipe when they depend on tasks from
another recipe. For example::

   SIGGEN_EXCLUDE_SAFE_RECIPE_DEPS += "intone->mplayer2"

In the previous example, ``intone`` depends on ``mplayer2``.

You can use the special token ``"*"`` on the left-hand side of the
dependency to match all recipes except the one on the right-hand
side. Here is an example::

   SIGGEN_EXCLUDE_SAFE_RECIPE_DEPS += "*->quilt-native"

In the previous example, all recipes except ``quilt-native`` ignore
task signatures from the ``quilt-native`` recipe when determining
their task signatures.

Use of this variable is one mechanism to remove dependencies that
affect task signatures and thus force rebuilds when a recipe changes.

.. note::

   If you add an inappropriate dependency for a recipe relationship,
   the software might break during runtime if the interface of the
   second recipe was changed after the first recipe had been built.
