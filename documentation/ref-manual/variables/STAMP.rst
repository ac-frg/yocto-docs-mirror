Specifies the base path used to create recipe stamp files. The path
to an actual stamp file is constructed by evaluating this string and
then appending additional information. Currently, the default
assignment for :term:`STAMP` as set in the ``meta/conf/bitbake.conf``
file is::

   STAMP = "${STAMPS_DIR}/${MULTIMACH_TARGET_SYS}/${PN}/${EXTENDPE}${PV}-${PR}"

For information on how BitBake uses stamp files to determine if a
task should be rerun, see the
":ref:`overview-manual/concepts:stamp files and the rerunning of tasks`"
section in the Yocto Project Overview and Concepts Manual.

See :term:`STAMPS_DIR`,
:term:`MULTIMACH_TARGET_SYS`,
:term:`PN`, :term:`EXTENDPE`,
:term:`PV`, and :term:`PR` for related variable
information.
