Specifies the version of the SDK. The Poky distribution configuration file
(``/meta-poky/conf/distro/poky.conf``) sets the default
:term:`SDK_VERSION` as follows::

   SDK_VERSION = "${@d.getVar('DISTRO_VERSION').replace('snapshot-${METADATA_REVISION}', 'snapshot')}"

For additional information, see the
:term:`DISTRO_VERSION` and
:term:`METADATA_REVISION` variables.
