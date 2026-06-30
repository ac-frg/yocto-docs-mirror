Used to prevent the OpenEmbedded build system from building a given
recipe. Specify the :term:`PN` value as a variable flag (``varflag``)
and provide a reason, which will be reported when attempting to
build the recipe.

To prevent a recipe from being built, use the :term:`SKIP_RECIPE`
variable in your ``local.conf`` file or distribution configuration.
Here is an example which prevents ``myrecipe`` from being built::

   SKIP_RECIPE[myrecipe] = "Not supported by our organization."
