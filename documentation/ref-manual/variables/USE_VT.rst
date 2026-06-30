When using
:ref:`SysVinit <dev-manual/new-recipe:enabling system services>`,
determines whether or not to run a :wikipedia:`getty <Getty_(Unix)>`
on any virtual terminals in order to enable logging in through those
terminals.

The default value used for :term:`USE_VT` is "1" when no default value is
specifically set. Typically, you would set :term:`USE_VT` to "0" in the
machine configuration file for machines that do not have a graphical
display attached and therefore do not need virtual terminal
functionality.
