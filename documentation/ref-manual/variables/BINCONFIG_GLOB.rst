When inheriting the :ref:`ref-classes-binconfig` class,
this variable specifies a wildcard for configuration scripts that
need editing. The scripts are edited to correct any paths that have
been set up during compilation so that they are correct for use when
installed into the sysroot and called by the build processes of other
recipes.

.. note::

   The :term:`BINCONFIG_GLOB` variable uses
   `shell globbing <https://tldp.org/LDP/abs/html/globbingref.html>`__,
   which is recognition and expansion of wildcards during pattern
   matching. Shell globbing is very similar to
   `fnmatch <https://docs.python.org/3/library/fnmatch.html#module-fnmatch>`__
   and `glob <https://docs.python.org/3/library/glob.html>`__.

For more information on how this variable works, see
``meta/classes-recipe/binconfig.bbclass`` in :term:`OpenEmbedded-Core
(OE-Core)`. You can also find general
information on the class in the
":ref:`ref-classes-binconfig`" section.
