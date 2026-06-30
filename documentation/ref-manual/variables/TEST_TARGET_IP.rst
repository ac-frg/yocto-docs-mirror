The IP address of your hardware under test. The :term:`TEST_TARGET_IP`
variable has no effect when :term:`TEST_TARGET` is
set to "qemu".

When you specify the IP address, you can also include a port. Here is
an example::

   TEST_TARGET_IP = "192.168.1.4:2201"

Specifying a port is
useful when SSH is started on a non-standard port or in cases when
your hardware under test is behind a firewall or network that is not
directly accessible from your host and you need to do port address
translation.
