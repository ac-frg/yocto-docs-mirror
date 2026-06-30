When inheriting the :ref:`ref-classes-pypi` class, specifies the
`PyPI <https://pypi.org/>`__ package name to be built. The default value
is set based upon :term:`BPN` (stripping any "python-" or "python3-"
prefix off if present), however for some packages it will need to be set
explicitly if that will not match the package name (e.g. where the
package name has a prefix, underscores, uppercase letters etc.)
