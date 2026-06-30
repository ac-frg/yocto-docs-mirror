The IP address of the build machine (host machine). This IP address
is usually automatically detected. However, if detection fails, this
variable needs to be set to the IP address of the build machine (i.e.
where the build is taking place).

.. note::

   The :term:`TEST_SERVER_IP` variable is only used for a small number of
   tests such as the "dnf" test suite, which needs to download packages
   from ``WORKDIR/oe-rootfs-repo``.
