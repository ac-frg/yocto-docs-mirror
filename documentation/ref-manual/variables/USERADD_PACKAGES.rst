When inheriting the :ref:`ref-classes-useradd` class,
this variable specifies the individual packages within the recipe
that require users and/or groups to be added.

You must set this variable if the recipe inherits the class. For
example, the following enables adding a user for the main package in
a recipe::

   USERADD_PACKAGES = "${PN}"

.. note::

   It follows that if you are going to use the :term:`USERADD_PACKAGES`
   variable, you need to set one or more of the :term:`USERADD_PARAM`,
   :term:`GROUPADD_PARAM`, or :term:`GROUPMEMS_PARAM` variables.
