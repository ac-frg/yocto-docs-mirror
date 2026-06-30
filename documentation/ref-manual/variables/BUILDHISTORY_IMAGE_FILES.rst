When inheriting the :ref:`ref-classes-buildhistory`
class, this variable specifies a list of paths to files copied from
the image contents into the build history directory under an
"image-files" directory in the directory for the image, so that you
can track the contents of each file. The default is to copy
``/etc/passwd`` and ``/etc/group``, which allows you to monitor for
changes in user and group entries. You can modify the list to include
any file. Specifying an invalid path does not produce an error.
Consequently, you can include files that might not always be present.

By default, the :ref:`ref-classes-buildhistory` class provides paths to
the following files::

   BUILDHISTORY_IMAGE_FILES ?= "/etc/passwd /etc/group"
