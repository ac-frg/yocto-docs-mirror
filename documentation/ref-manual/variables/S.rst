The location in the :term:`Build Directory` where
unpacked recipe source code resides. By default, this directory is
``${``\ :term:`UNPACKDIR`\ ``}/${``\ :term:`BPN`\ ``}-${``\ :term:`PV`\ ``}``,
where ``${BPN}`` is the base recipe name and ``${PV}`` is the recipe
version. If the source tarball extracts the code to a directory named
anything other than ``${BPN}-${PV}``, or if the source code is
fetched from an SCM such as Git or Subversion, then you must set
:term:`S` in the recipe so that the OpenEmbedded build system knows where
to find the unpacked source.

As an example, assume a :term:`Source Directory`
top-level folder named ``bitbake-builds`` and a default :term:`Build Directory` at
``bitbake-builds/build``. In this case, the work directory the build system
uses to keep the unpacked recipe for ``db`` is the following::

   bitbake-builds/build/tmp/work/qemux86-poky-linux/db/5.1.19-r3/sources/db-5.1.19

The unpacked source code resides in the ``db-5.1.19`` folder.
