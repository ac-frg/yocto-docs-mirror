When using ``runqemu``, the :term:`QB_TAP_OPT` variable controls
the network option for "tap" mode.

For example::

   QB_TAP_OPT = "-netdev tap,id=net0,ifname=@TAP@,script=no,downscript=no"

Note that ``runqemu`` will replace ``@TAP@`` with the tap interface in
use, such as ``tap0``, ``tap1``, etc.
