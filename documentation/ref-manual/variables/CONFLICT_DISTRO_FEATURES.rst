When inheriting the :ref:`ref-classes-features_check`
class, this variable identifies distro features that would be
in conflict should the recipe be built. In other words, if the
:term:`CONFLICT_DISTRO_FEATURES` variable lists a feature that also
appears in :term:`DISTRO_FEATURES` within the current configuration, then
the recipe will be skipped, and if the build system attempts to build
the recipe then an error will be triggered.
