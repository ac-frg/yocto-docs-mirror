When using ``runqemu``, the :term:`QB_NETWORK_DEVICE` variable controls
the network device instantiated by QEMU. This value needs to be compatible
with the :term:`QB_TAP_OPT` variable.

Example::

   QB_NETWORK_DEVICE = "-device virtio-net-pci,netdev=net0,mac=@MAC@"

``runqemu`` replaces ``@MAC@`` with a predefined mac address.
