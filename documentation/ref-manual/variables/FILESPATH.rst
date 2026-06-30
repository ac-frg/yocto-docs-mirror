A colon-separated list specifying the default set of directories the
OpenEmbedded build system uses when searching for patches and files.

During the build process, BitBake searches each directory in
:term:`FILESPATH` in the specified order when looking for files and
patches specified by each ``file://`` URI in a recipe's
:term:`SRC_URI` statements.

The default value for the :term:`FILESPATH` variable is defined in the
:ref:`ref-classes-base` class found in ``meta/classes-global`` in
:term:`OpenEmbedded-Core (OE-Core)`::

   FILESPATH = "${@base_set_filespath(["${FILE_DIRNAME}/${BP}", \
       "${FILE_DIRNAME}/${BPN}", "${FILE_DIRNAME}/files"], d)}"

The
:term:`FILESPATH` variable is automatically extended using the overrides
from the :term:`FILESOVERRIDES` variable.

.. note::

   -  Do not hand-edit the :term:`FILESPATH` variable. If you want the
      build system to look in directories other than the defaults,
      extend the :term:`FILESPATH` variable by using the
      :term:`FILESEXTRAPATHS` variable.

   -  Be aware that the default :term:`FILESPATH` directories do not map
      to directories in custom layers where append files
      (``.bbappend``) are used. If you want the build system to find
      patches or files that reside with your append files, you need
      to extend the :term:`FILESPATH` variable by using the
      :term:`FILESEXTRAPATHS` variable.

You can take advantage of this searching behavior in useful ways. For
example, consider a case where there is the following directory structure
for general and machine-specific configurations::

   files/defconfig
   files/MACHINEA/defconfig
   files/MACHINEB/defconfig

Also in the example, the :term:`SRC_URI` statement contains
"file://defconfig". Given this scenario, you can set
:term:`MACHINE` to "MACHINEA" and cause the build
system to use files from ``files/MACHINEA``. Set :term:`MACHINE` to
"MACHINEB" and the build system uses files from ``files/MACHINEB``.
Finally, for any machine other than "MACHINEA" and "MACHINEB", the
build system uses files from ``files/defconfig``.

You can find out more about the patching process in the
":ref:`overview-manual/concepts:patching`" section
in the Yocto Project Overview and Concepts Manual and the
":ref:`dev-manual/new-recipe:patching code`" section in
the Yocto Project Development Tasks Manual. See the
:term:`do_patch` task as well.
