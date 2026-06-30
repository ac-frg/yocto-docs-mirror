When inheriting the :ref:`ref-classes-useradd` class,
this variable specifies for a package what parameters should pass to
the ``useradd`` command if you add a user to the system when the
package is installed.

Here is an example from the ``dbus`` recipe::

   USERADD_PARAM:${PN} = "--system --home ${localstatedir}/lib/dbus \
                          --no-create-home --shell /bin/false \
                          --user-group messagebus"

For information on the
standard Linux shell command ``useradd``, see
https://linux.die.net/man/8/useradd.
