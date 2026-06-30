Specifies a recommendation for why a directory must be empty,
which will be included in the error message if a specific directory
is found to contain files. Must be overridden with the directory
path to match on.

If no recommendation is specified for a directory, then the default
"but it is expected to be empty" will be used.

An example message shows if files were present in '/dev'::

   QA_EMPTY_DIRS_RECOMMENDATION:/dev = "but all devices must be created at runtime"
