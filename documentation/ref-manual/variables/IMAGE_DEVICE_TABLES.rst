Specifies one or more files that contain custom device tables that
are passed to the ``makedevs`` command as part of creating an image.
These files list basic device nodes that should be created under
``/dev`` within the image. If :term:`IMAGE_DEVICE_TABLES` is not set,
``files/device_table-minimal.txt`` is used, which is located by
:term:`BBPATH`. For details on how you should write
device table files, see ``meta/files/device_table-minimal.txt`` as an
example.
