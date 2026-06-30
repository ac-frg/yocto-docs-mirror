When inheriting the :ref:`ref-classes-pypi` class, specifies the
full `pythonhosted <https://files.pythonhosted.org/>`__ URI for
fetching the package to be built. The default value is constructed
based upon :term:`PYPI_PACKAGE`, :term:`PYPI_PACKAGE_EXT`, and
:term:`PV`. Most recipes will not need to set this variable unless
they are building an unstable (i.e. development) version.
