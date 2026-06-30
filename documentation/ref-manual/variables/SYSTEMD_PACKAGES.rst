When inheriting the :ref:`ref-classes-systemd` class,
this variable locates the systemd unit files when they are not found
in the main recipe's package. By default, the :term:`SYSTEMD_PACKAGES`
variable is set such that the systemd unit files are assumed to
reside in the recipes main package::

   SYSTEMD_PACKAGES ?= "${PN}"

If these unit files are not in this recipe's main package, you need
to use :term:`SYSTEMD_PACKAGES` to list the package or packages in which
the build system can find the systemd unit files.
