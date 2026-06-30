When using ``runqemu``, the :term:`QB_RNG` variable controls
pass-through for host random number generator, it can speedup boot
in system mode, where system is experiencing entropy starvation.

For example::

   QB_RNG = "-object rng-random,filename=/dev/urandom,id=rng0 -device virtio-rng-pci,rng=rng0"
