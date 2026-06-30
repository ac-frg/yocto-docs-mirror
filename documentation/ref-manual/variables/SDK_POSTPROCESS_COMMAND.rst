Specifies a list of functions to call once the OpenEmbedded build
system creates the SDK. You can specify functions separated by
spaces:

   SDK_POSTPROCESS_COMMAND += "function"

If you need to pass an SDK path to a command within a function, you
can use ``${SDK_DIR}``, which points to the parent directory used by
the OpenEmbedded build system when creating SDK output. See the
:term:`SDK_DIR` variable for more information.
