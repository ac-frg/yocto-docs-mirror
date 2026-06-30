The version of the recipe. The version is normally extracted from the
recipe filename. For example, if the recipe is named
``expat_2.0.1.bb``, then the default value of :term:`PV` will be "2.0.1".
:term:`PV` is generally not overridden within a recipe unless it is
building an unstable (i.e. development) version from a source code
repository (e.g. Git or Subversion).

:term:`PV` is the default value of the :term:`PKGV` variable.
