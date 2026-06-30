The variable :term:`SRCPV` is deprecated. It was previously used to
include source control information in :term:`PV` for :term:`bitbake` to
work correctly but this is no longer a requirement. Source control
information will be automatically included by :term:`bitbake` in the
variable :term:`PKGV` during packaging if the ``+`` sign is present in
:term:`PV`.

.. note::

   The :term:`SRCPV` variable used to be defined in the
   ``meta/conf/bitbake.conf`` configuration file in
   :term:`OpenEmbedded-Core (OE-Core)` as follows::

      SRCPV = "${@bb.fetch2.get_srcrev(d)}"

   The ``get_srcrev`` function can still be used to include source control
   information in variables manually.
