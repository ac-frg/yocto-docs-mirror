A space-separated list of configuration options generated from the
:term:`PACKAGECONFIG` setting.

Classes such as :ref:`ref-classes-autotools` and :ref:`ref-classes-cmake`
use :term:`PACKAGECONFIG_CONFARGS` to pass :term:`PACKAGECONFIG` options
to ``configure`` and ``cmake``, respectively. If you are using
:term:`PACKAGECONFIG` but not a class that handles the
:term:`do_configure` task, then you need to use
:term:`PACKAGECONFIG_CONFARGS` appropriately.
