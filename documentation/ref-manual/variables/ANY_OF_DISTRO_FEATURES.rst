When inheriting the :ref:`ref-classes-features_check`
class, this variable identifies a list of distribution features where
at least one must be enabled in the current configuration in order
for the OpenEmbedded build system to build the recipe. In other words,
if none of the features listed in :term:`ANY_OF_DISTRO_FEATURES`
appear in :term:`DISTRO_FEATURES` within the current configuration, then
the recipe will be skipped, and if the build system attempts to build
the recipe then an error will be triggered.
