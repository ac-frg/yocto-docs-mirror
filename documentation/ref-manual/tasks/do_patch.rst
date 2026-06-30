Locates patch files and applies them to the source code.

After fetching and unpacking source files, the build system uses the
recipe's :term:`SRC_URI` statements
to locate and apply patch files to the source code.

.. note::

   The build system uses the :term:`FILESPATH` variable to determine the
   default set of directories when searching for patches.

Patch files, by default, are ``*.patch`` and ``*.diff`` files created
and kept in a subdirectory of the directory holding the recipe file. For
example, consider the
:oe_git:`bluez5 </openembedded-core/tree/meta/recipes-connectivity/bluez5>`
recipe from the :term:`OpenEmbedded-Core (OE-Core)` layer::

   meta/recipes-connectivity/bluez5

This recipe has two patch files located here::

   meta/recipes-connectivity/bluez5/bluez5

In the ``bluez5`` recipe, the :term:`SRC_URI` statements point to the source
and patch files needed to build the package.

.. note::

   In the case for the ``bluez5_5.48.bb`` recipe, the :term:`SRC_URI` statements
   are from an include file ``bluez5.inc``.

As mentioned earlier, the build system treats files whose file types are
``.patch`` and ``.diff`` as patch files. However, you can use the
"apply=yes" parameter with the :term:`SRC_URI` statement to indicate any
file as a patch file::

   SRC_URI = " \
       git://path_to_repo/some_package \
       file://file;apply=yes \
       "

Conversely, if you have a file whose file type is ``.patch`` or ``.diff``
and you want to exclude it so that the :term:`do_patch` task does not apply
it during the patch phase, you can use the "apply=no" parameter with the
:term:`SRC_URI` statement::

   SRC_URI = " \
       git://path_to_repo/some_package \
       file://file1.patch \
       file://file2.patch;apply=no \
       "

In the previous example ``file1.patch`` would be applied as a patch by default
while ``file2.patch`` would not be applied.

You can find out more about the patching process in the
":ref:`overview-manual/concepts:patching`" section in
the Yocto Project Overview and Concepts Manual and the
":ref:`dev-manual/new-recipe:patching code`" section in the
Yocto Project Development Tasks Manual.
