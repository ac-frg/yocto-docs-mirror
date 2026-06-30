Features used to "tune" a compiler for optimal use given a specific
processor. The features are defined within the tune files and allow
arguments (i.e. ``TUNE_*ARGS``) to be dynamically generated based on
the features.

The OpenEmbedded build system verifies the features to be sure they
are not conflicting and that they are supported.

The BitBake configuration file (``meta/conf/bitbake.conf``) defines
:term:`TUNE_FEATURES` as follows::

   TUNE_FEATURES ??= "${TUNE_FEATURES:tune-${DEFAULTTUNE}}"

See the :term:`DEFAULTTUNE` variable for more information.
