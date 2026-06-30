A colon-separated list to extend the search path the OpenEmbedded build
system uses when looking for files and patches as it processes recipes
and append files. The default directories BitBake uses when it processes
recipes are initially defined by the :term:`FILESPATH` variable. You can
extend :term:`FILESPATH` variable by using :term:`FILESEXTRAPATHS`.

Best practices dictate that you accomplish this by using
:term:`FILESEXTRAPATHS` from within a ``.bbappend`` file and that you
prepend paths as follows::

   FILESEXTRAPATHS:prepend := "${THISDIR}/${PN}:"

In the above example, the build system first
looks for files in a directory that has the same name as the
corresponding append file.

.. note::

   When extending :term:`FILESEXTRAPATHS`, be sure to use the immediate
   expansion (``:=``) operator. Immediate expansion makes sure that
   BitBake evaluates :term:`THISDIR` at the time the
   directive is encountered rather than at some later time when
   expansion might result in a directory that does not contain the
   files you need.

   Also, include the trailing separating colon character if you are
   prepending. The trailing colon character is necessary because you
   are directing BitBake to extend the path by prepending directories
   to the search path.

Here is another common use::

   FILESEXTRAPATHS:prepend := "${THISDIR}/files:"

In this example, the build system extends the
:term:`FILESPATH` variable to include a directory named ``files`` that is
in the same directory as the corresponding append file.

This next example specifically adds three paths::

   FILESEXTRAPATHS:prepend := "path_1:path_2:path_3:"

A final example shows how you can extend the search path and include
a :term:`MACHINE`-specific override, which is useful
in a BSP layer::

    FILESEXTRAPATHS:prepend:intel-x86-common := "${THISDIR}/${PN}:"

The previous statement appears in the
``linux-yocto-dev.bbappend`` file, which is found in the
:ref:`overview-manual/development-environment:yocto project source repositories` in
``meta-intel/common/recipes-kernel/linux``. Here, the machine
override is a special :term:`PACKAGE_ARCH`
definition for multiple ``meta-intel`` machines.

.. note::

   For a layer that supports a single BSP, the override could just be
   the value of :term:`MACHINE`.

By prepending paths in ``.bbappend`` files, you allow multiple append
files that reside in different layers but are used for the same
recipe to correctly extend the path.
