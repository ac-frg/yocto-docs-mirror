For recipes inheriting the
:ref:`ref-classes-update-rc.d` class, :term:`UPDATERCPN`
specifies the package that contains the initscript that is enabled.

The default value is "${PN}". Given that almost all recipes that
install initscripts package them in the main package for the recipe,
you rarely need to set this variable in individual recipes.
