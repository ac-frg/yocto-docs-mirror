When inheriting the :ref:`ref-classes-useradd` class,
this variable specifies for a package what parameters should be
passed to the ``groupadd`` command if you wish to add a group to the
system when the package is installed.

Here is an example from the ``dbus`` recipe::

   GROUPADD_PARAM:${PN} = "-r netdev"

More than one group can be added by separating each set of different
groups' parameters with a semicolon.

Here is an example adding multiple groups from the ``useradd-example.bb``
file in the ``meta-skeleton`` layer::

   GROUPADD_PARAM:${PN} = "-g 880 group1; -g 890 group2"

For information on the standard Linux shell command
``groupadd``, see https://linux.die.net/man/8/groupadd.
