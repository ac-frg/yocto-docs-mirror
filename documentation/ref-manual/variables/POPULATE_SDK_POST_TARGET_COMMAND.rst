Specifies a list of functions to call once the OpenEmbedded build
system has created the target part of the SDK. You can specify
functions separated by spaces::

   POPULATE_SDK_POST_TARGET_COMMAND += "function"

If you need to pass the SDK path to a command within a function, you
can use ``${SDK_DIR}``, which points to the parent directory used by
the OpenEmbedded build system when creating SDK output. See the
:term:`SDK_DIR` variable for more information.
