Defines the file specification to match
:term:`SOLIBSDEV`. In other words,
:term:`FILES_SOLIBSDEV` defines the full path name of the development
symbolic link (symlink) for shared libraries on the target platform.

The following statement from the ``bitbake.conf`` shows how it is
set::

   FILES_SOLIBSDEV ?= "${base_libdir}/lib*${SOLIBSDEV} ${libdir}/lib*${SOLIBSDEV}"
