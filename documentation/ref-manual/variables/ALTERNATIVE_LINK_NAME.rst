Used by the alternatives system to map duplicated commands to actual
locations. For example, if the ``bracket`` command provided by the
``busybox`` package is duplicated through another package, you must
use the :term:`ALTERNATIVE_LINK_NAME` variable to specify the actual
location::

   ALTERNATIVE_LINK_NAME[bracket] = "/usr/bin/["

In this example, the binary for the ``bracket`` command (i.e. ``[``)
from the ``busybox`` package resides in ``/usr/bin/``.

.. note::

   If :term:`ALTERNATIVE_LINK_NAME` is not defined, it defaults to ``${bindir}/name``.

For more information on the alternatives system, see the
":ref:`ref-classes-update-alternatives`"
section.
