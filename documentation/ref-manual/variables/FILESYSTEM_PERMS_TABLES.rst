Allows you to define your own file permissions settings tables as part
of your configuration for the packaging process. For example, suppose
you need a consistent set of custom permissions for a set of groups
and users across an entire work project. It is best to do this in the
packages themselves but this is not always possible.

By default, the OpenEmbedded build system uses the ``fs-perms.txt``,
``fs-perms-volatile-log.txt`` and ``fs-perms-volatile-tmp.txt`` which are
located in the ``meta/files`` folder in :term:`OpenEmbedded-Core (OE-Core)`. If
you create your own permission setting table files, you should place
those in your layer.

You can override the value of :term:`FILESYSTEM_PERMS_TABLES` variable
in your distribution configuration file to point to your custom
permission table files. You can specify one or more file permissions
setting tables. The paths that you specify to these files must be defined
within the :term:`BBPATH` variable.

In order to disable the volatile log, which is enabled by default, one
can remove the ``files/fs-perms-volatile-log.txt`` value from
``FILESYSTEM_PERMS_TABLES``. Similarly, in order to disable the volatile
tmp, one can remove the ``files/fs-perms-volatile-tmp.txt`` value.

For guidance on how to define your own file permissions settings
tables, examine the existing ``fs-perms.txt``,
``fs-perms-volatile-log.txt`` and ``fs-perms-volatile-tmp.txt`` files.
