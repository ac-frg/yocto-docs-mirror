Directories that are not staged into the sysroot by the
:term:`do_populate_sysroot` task. You
can use this variable to exclude certain subdirectories of
directories listed in :term:`SYSROOT_DIRS` from
staging. By default, the following directories are not staged::

   SYSROOT_DIRS_IGNORE = " \
       ${mandir} \
       ${docdir} \
       ${infodir} \
       ${datadir}/X11/locale \
       ${datadir}/applications \
       ${datadir}/bash-completion \
       ${datadir}/fonts \
       ${datadir}/gtk-doc/html \
       ${datadir}/installed-tests \
       ${datadir}/locale \
       ${datadir}/pixmaps \
       ${datadir}/terminfo \
       ${libdir}/${BPN}/ptest \
       "
