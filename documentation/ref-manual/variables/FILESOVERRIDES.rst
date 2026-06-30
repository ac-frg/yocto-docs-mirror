A colon-separated list to specify a subset of :term:`OVERRIDES` used by
the OpenEmbedded build system for creating :term:`FILESPATH`. The
:term:`FILESOVERRIDES` variable uses overrides to automatically extend
the :term:`FILESPATH` variable. For an example of how that works, see the
:term:`FILESPATH` variable description. Additionally, you find more
information on how overrides are handled in the
":ref:`bitbake-user-manual/bitbake-user-manual-metadata:conditional syntax (overrides)`"
section of the BitBake User Manual.

By default, the :term:`FILESOVERRIDES` variable is defined as::

   FILESOVERRIDES = "${TRANSLATED_TARGET_ARCH}:${MACHINEOVERRIDES}:${DISTROOVERRIDES}"

.. note::

   Do not hand-edit the :term:`FILESOVERRIDES` variable. The values match up
   with expected overrides and are used in an expected manner by the
   build system.
