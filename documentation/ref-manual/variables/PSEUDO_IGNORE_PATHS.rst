A comma-separated (without spaces) list of path prefixes that should be ignored
by pseudo when monitoring and recording file operations, in order to avoid
problems with files being written to outside of the pseudo context and
reduce pseudo's overhead. A path is ignored if it matches any prefix in the list
and can include partial directory (or file) names. In case a path prefix is
present in both :term:`PSEUDO_IGNORE_PATHS` and in :term:`PSEUDO_INCLUDE_PATHS`,
:term:`PSEUDO_INCLUDE_PATHS` takes precedence.
