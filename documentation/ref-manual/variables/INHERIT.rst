Causes the named class or classes to be inherited globally. Anonymous
functions in the class or classes are not executed for the base
configuration and in each individual recipe. The OpenEmbedded build
system ignores changes to :term:`INHERIT` in individual recipes.
Classes inherited using :term:`INHERIT` must be located in the
``classes-global/`` or ``classes/`` subdirectories.

For more information on :term:`INHERIT`, see the
:ref:`bitbake-user-manual/bitbake-user-manual-metadata:\`\`inherit\`\` configuration directive`"
section in the BitBake User Manual.
