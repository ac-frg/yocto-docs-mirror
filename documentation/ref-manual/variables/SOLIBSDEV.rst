Defines the suffix for the development symbolic link (symlink) for
shared libraries on the target platform. By default, this suffix is
".so" for Linux-based systems and is defined in the
``meta/conf/bitbake.conf`` configuration file.

You will see this variable referenced in the default values of
``FILES:${PN}-dev``.
