Specifies a weak bias for recipe selection priority.

The most common usage of this is variable is to set it to "-1" within
a recipe for a development version of a piece of software. Using the
variable in this way causes the stable version of the recipe to build
by default in the absence of :term:`PREFERRED_VERSION` being used to
build the development version.

.. note::

   The bias provided by :term:`DEFAULT_PREFERENCE` is weak and is overridden
   by :term:`BBFILE_PRIORITY` if that variable is different between two
   layers that contain different versions of the same recipe.
