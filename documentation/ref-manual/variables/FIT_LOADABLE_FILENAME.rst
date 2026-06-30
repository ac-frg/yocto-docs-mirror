Filename (or relative path) for the loadables defined in
:term:`FIT_LOADABLES`; this will be used to search for the binary to
include and is therefore mandatory for each loadable. Binary files to be
included need to be located in :term:`DEPLOY_DIR_IMAGE`.

This variable cannot be used directly, but only defining flags on it.

Example::

   FIT_LOADABLES = "foo"
   FIT_LOADABLE_FILENAME[foo] = "foo-firmware.bin"
