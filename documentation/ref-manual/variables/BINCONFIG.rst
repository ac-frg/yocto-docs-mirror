When inheriting the :ref:`ref-classes-binconfig-disabled` class, this
variable specifies binary configuration scripts to disable in favor of
using ``pkg-config`` to query the information. The
:ref:`ref-classes-binconfig-disabled` class will modify the specified
scripts to return an error so that calls to them can be easily found
and replaced.

To add multiple scripts, separate them by spaces. Here is an example
from the ``libpng`` recipe::

   BINCONFIG = "${bindir}/libpng-config ${bindir}/libpng16-config"
