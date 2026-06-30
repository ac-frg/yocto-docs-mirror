The :term:`PREFERRED_RPROVIDER` variable works like the
:term:`PREFERRED_PROVIDER` variable, but it denotes packages that provide a
*runtime* component. Runtime providers are declared in recipes that set
the :term:`RPROVIDES` variable for a specific package.

For example::

   PREFERRED_RPROVIDER_virtual-x-terminal-emulator = "rxvt-unicode"

This statement sets the runtime provider for the X terminal emulator to
``rxvt-unicode``. The ``rxvt-unicode`` package is a runtime provider of
this component because the ``rxvt-unicode`` recipe set the following
:term:`RPROVIDES` definition for the ``rxvt-unicode`` (``${PN}``)
package::

   RPROVIDES:${PN} = "virtual-x-terminal-emulator"

For more information on virtual providers, see the
":ref:`dev-manual/new-recipe:using virtual providers`" section in the
Yocto Project Development Tasks Manual.
