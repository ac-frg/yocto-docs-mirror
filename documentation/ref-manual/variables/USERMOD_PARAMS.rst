When a recipe inherits the :ref:`ref-classes-useradd` class, this variable
specifies for a package what parameters should be passed to the ``usermod``
command if you wish to modify a user when the package is installed.
Is is typically used to add the user to one or more groups. For example::

   USERMOD_PARAM:${PN} = "--append --groups group1,group2 user"
