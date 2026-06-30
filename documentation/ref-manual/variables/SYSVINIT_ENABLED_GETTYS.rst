When using :ref:`SysVinit <dev-manual/new-recipe:enabling system services>`,
specifies a space-separated list of the virtual terminals that should
run a :wikipedia:`getty <Getty_(Unix)>` (allowing login), assuming
:term:`USE_VT` is not set to "0".

The default value for :term:`SYSVINIT_ENABLED_GETTYS` is "1" (i.e. only
run a getty on the first virtual terminal).
