When inheriting the :ref:`ref-classes-fontcache` class, this variable
identifies packages containing font files that need to be cached by
Fontconfig. By default, the :ref:`ref-classes-fontcache` class assumes
that fonts are in the recipe's main package (i.e.
``${``\ :term:`PN`\ ``}``). Use this variable if fonts you
need are in a package other than that main package.
