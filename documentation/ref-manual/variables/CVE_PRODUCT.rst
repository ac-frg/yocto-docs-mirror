In a recipe, defines the name used to match the recipe name
against the name in the upstream `NIST CVE database <https://nvd.nist.gov/>`__.

The default is ${:term:`BPN`} (except for recipes that inherit the
:ref:`ref-classes-pypi` class where it is set based upon
:term:`PYPI_PACKAGE`). If it does not match the name in the NIST CVE
database or matches with multiple entries in the database, the default
value needs to be changed.

Here is an example from the :oe_layerindex:`Berkeley DB recipe </layerindex/recipe/544>`::

   CVE_PRODUCT = "oracle_berkeley_db berkeley_db"

Sometimes the product name is not specific enough, for example
"tar" has been matching CVEs for the GNU ``tar`` package and also
the ``node-tar`` node.js extension. To avoid this problem, use the
vendor name as a prefix. The syntax for this is::

   CVE_PRODUCT = "vendor:package"

Since Wrynose (6.0), special characters must not be escaped. For example,
the :term:`CVE_PRODUCT` variable for the ``webkitgtk`` recipe must no
longer be written as ``webkitgtk\+`` but rather ``webkitgtk+``.
