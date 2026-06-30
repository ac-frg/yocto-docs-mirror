Specifies the by default machine-specific suffix for image file names
(before the extension). The default value is set as follows::

   IMAGE_MACHINE_SUFFIX ??= "-${MACHINE}"

The default :term:`DEPLOY_DIR_IMAGE` already has a :term:`MACHINE`
subdirectory, so you may find it unnecessary to also include this suffix
in the name of every image file. If you prefer to remove the suffix you
can set this variable to an empty string::

   IMAGE_MACHINE_SUFFIX = ""

(Not to be confused with :term:`IMAGE_NAME_SUFFIX`.)
