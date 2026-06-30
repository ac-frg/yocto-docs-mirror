When used by recipes that inherit the :ref:`ref-classes-setuptools3`
class, this variable should be used to specify the directory in which
the ``setup.py`` file is located if it is not at the root of the source
tree (as specified by :term:`S`). For example, in a recipe where the
sources are fetched from a Git repository and ``setup.py`` is in a
``python/pythonmodule`` subdirectory, you would have this::

   SETUPTOOLS_SETUP_PATH = "${S}/python/pythonmodule"
