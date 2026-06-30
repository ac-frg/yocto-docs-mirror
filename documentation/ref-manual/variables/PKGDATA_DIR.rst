Points to a shared, global-state directory that holds data generated
during the packaging process. During the packaging process, the
:term:`do_packagedata` task packages data
for each recipe and installs it into this shared area.
This directory defaults to the following, which you should not
change::

   ${TMPDIR}/pkgdata/${MACHINE}

For examples of how this data is used, see the
":ref:`overview-manual/concepts:automatically added runtime dependencies`"
section in the Yocto Project Overview and Concepts Manual and the
":ref:`dev-manual/debugging:viewing package information with ``oe-pkgdata-util```"
section in the Yocto Project Development Tasks Manual.
