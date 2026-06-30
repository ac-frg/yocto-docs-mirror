The list of packages the recipe creates. The default value is the
following::

   ${PN}-src ${PN}-dbg ${PN}-staticdev ${PN}-dev ${PN}-doc ${PN}-locale ${PACKAGE_BEFORE_PN} ${PN}

During packaging, the :term:`do_package` task
goes through :term:`PACKAGES` and uses the :term:`FILES`
variable corresponding to each package to assign files to the
package. If a file matches the :term:`FILES` variable for more than one
package in :term:`PACKAGES`, it will be assigned to the earliest
(leftmost) package.

Packages in the variable's list that are empty (i.e. where none of
the patterns in ``FILES:``\ pkg match any files installed by the
:term:`do_install` task) are not generated,
unless generation is forced through the
:term:`ALLOW_EMPTY` variable.
