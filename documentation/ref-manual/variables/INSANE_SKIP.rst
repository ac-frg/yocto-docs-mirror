Specifies the QA checks to skip for a specific package within a
recipe. For example, to skip the check for symbolic link ``.so``
files in the main package of a recipe, add the following to the
recipe. The package name override must be used, which in this example
is ``${PN}``::

   INSANE_SKIP:${PN} += "dev-so"

See the ":ref:`ref-classes-insane`" section for a
list of the valid QA checks you can specify using this variable.
