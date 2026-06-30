Extra options passed to the build tool install command
(``make install``, ``ninja install`` or more specific ones)
during the :term:`do_install` task in order to specify
parallel installation. This variable defaults to the value of
:term:`PARALLEL_MAKE`.

.. note::

   For software compiled by ``make``, in order for :term:`PARALLEL_MAKEINST`
   to be effective, ``make`` must be called with
   ``${``\ :term:`EXTRA_OEMAKE`\ ``}``. An easy
   way to ensure this is to use the ``oe_runmake`` function.

   If the software being built experiences dependency issues during
   the :term:`do_install` task that result in race conditions, you can
   clear the :term:`PARALLEL_MAKEINST` variable within the recipe as a
   workaround. For information on addressing race conditions, see the
   ":ref:`dev-manual/debugging:debugging parallel make races`"
   section in the Yocto Project Development Tasks Manual.
