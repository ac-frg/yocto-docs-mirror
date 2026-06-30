When using ``runqemu``, the :term:`QB_SMP` variable controls
amount of CPU cores made availalble inside the QEMU guest, each mapped to
a thread on the host.

For example::

   QB_SMP = "-smp 8".
