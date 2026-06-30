When inheriting the :ref:`ref-classes-features_check` class, this variable
identifies tune features that must exist in the current configuration in
order for the :term:`OpenEmbedded Build System` to build the recipe. In
other words, if the :term:`REQUIRED_TUNE_FEATURES` variable lists a
feature that does not appear in :term:`TUNE_FEATURES` within the current
configuration, then the recipe will be skipped, and if the build system
attempts to build the recipe then an error will be triggered.
