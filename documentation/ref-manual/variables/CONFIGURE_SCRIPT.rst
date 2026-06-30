When using the :ref:`ref-classes-autotools` class, the
:term:`CONFIGURE_SCRIPT` variable stores the location of the ``configure``
script for the Autotools build system. The default definition for this
variable is::

   CONFIGURE_SCRIPT ?= "${AUTOTOOLS_SCRIPT_PATH}/configure"

Where :term:`AUTOTOOLS_SCRIPT_PATH` is the location of the of the
Autotools build system scripts, which defaults to :term:`S`.
