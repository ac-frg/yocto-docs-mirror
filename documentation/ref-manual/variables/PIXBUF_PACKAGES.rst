When inheriting the :ref:`ref-classes-pixbufcache`
class, this variable identifies packages that contain the pixbuf
loaders used with ``gdk-pixbuf``. By default, the
:ref:`ref-classes-pixbufcache` class assumes that
the loaders are in the recipe's main package (i.e.
``${``\ :term:`PN`\ ``}``). Use this variable if the
loaders you need are in a package other than that main package.
