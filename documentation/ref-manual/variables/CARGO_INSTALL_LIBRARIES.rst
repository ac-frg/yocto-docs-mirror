When inheriting the :ref:`ref-classes-cargo` class, the variable
:term:`CARGO_INSTALL_LIBRARIES` can be set to a non-empty value by
individual recipes to enable the installation of the libraries the
recipe has built in ``${B}/target/${CARGO_TARGET_SUBDIR}`` (files ending
with ``.so`` or ``.rlib``). By default this variable is not defined and
libraries are not installed, to replicate the behavior of the ``cargo
install`` command.
