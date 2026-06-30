A colon-separated list of overrides that currently apply. Overrides
are a BitBake mechanism that allows variables to be selectively
overridden at the end of parsing. The set of overrides in
:term:`OVERRIDES` represents the "state" during building, which includes
the current recipe being built, the machine for which it is being
built, and so forth.

As an example, if the string "an-override" appears as an element in
the colon-separated list in :term:`OVERRIDES`, then the following
assignment will override ``FOO`` with the value "overridden" at the
end of parsing::

   FOO:an-override = "overridden"

See the
":ref:`bitbake-user-manual/bitbake-user-manual-metadata:conditional syntax (overrides)`"
section in the BitBake User Manual for more information on the
overrides mechanism.

The default value of :term:`OVERRIDES` includes the values of the
:term:`CLASSOVERRIDE`,
:term:`MACHINEOVERRIDES`, and
:term:`DISTROOVERRIDES` variables. Another
important override included by default is ``pn-${PN}``. This override
allows variables to be set for a single recipe within configuration
(``.conf``) files. Here is an example::

   FOO:pn-myrecipe = "myrecipe-specific value"

.. note::

   An easy way to see what overrides apply is to run the command
   ``bitbake-getvar -r myrecipe OVERRIDES``. See the
   ":ref:`dev-manual/debugging:viewing variable values`" section in the Yocto
   Project Development Tasks Manual for more information.
