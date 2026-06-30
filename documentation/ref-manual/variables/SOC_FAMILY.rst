A colon-separated list grouping together machines based upon the same
family of SoC (System On Chip). You typically set this variable in a
common ``.inc`` file that you include in the configuration files of all
the machines.

.. note::

   You must include ``conf/machine/include/soc-family.inc`` for this
   variable to appear in :term:`MACHINEOVERRIDES`.
