When upgrading a recipe with ``devtool upgrade``, the variable
:term:`RECIPE_UPGRADE_EXTRA_TASKS` specifies a space-delimited list of
tasks to run after the new sources have been unpacked.

For some recipes, after the new source has been unpacked, additional tasks
may need to be run during an upgrade. A good example of this is recipes
which inherit :ref:`ref-classes-cargo-update-recipe-crates`, where the
`do_update_crates` task needs to be run whenever Cargo.toml/Cargo.lock have
changed in the source.
