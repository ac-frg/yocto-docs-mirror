Specifies a list of dependencies for post-installation and
pre-installation scripts on native/cross tools. If your
post-installation or pre-installation script can execute at root filesystem
creation time rather than on the target but depends on a native tool
in order to execute, you need to list the tools in
:term:`PACKAGE_WRITE_DEPS`.

For information on running post-installation scripts, see the
":ref:`dev-manual/new-recipe:post-installation scripts`"
section in the Yocto Project Development Tasks Manual.
