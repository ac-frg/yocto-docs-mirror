This variable is similar to the :term:`QB_CMDLINE_IP_SLIRP` variable.

Use as follows::

   QB_CMDLINE_IP_TAP = "ip=192.168.7.@CLIENT@::192.168.7.@GATEWAY@:255.255.255.0::eth0"

Since the tap interface requires static IP configuration, ``runqemu``
replaces the ``@CLIENT@`` and ``@GATEWAY@`` place holders by the IP and
the gateway address of the QEMU guest.
