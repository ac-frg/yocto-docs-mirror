A list of variables not allowed through from the OpenEmbedded build
system configuration into the extensible SDK configuration. Usually,
these are variables that are specific to the machine on which the
build system is running and thus would be potentially problematic
within the extensible SDK.

By default, :term:`ESDK_LOCALCONF_REMOVE` is set in the
:ref:`populate-sdk-ext <ref-classes-populate-sdk-*>` class and
excludes the following variables:

- :term:`CONF_VERSION`
- :term:`BB_NUMBER_THREADS`
- :term:`BB_NUMBER_PARSE_THREADS`
- :term:`PARALLEL_MAKE`
- :term:`PRSERV_HOST`
- :term:`SSTATE_MIRRORS` :term:`DL_DIR`
- :term:`SSTATE_DIR` :term:`TMPDIR`
- :term:`BB_SERVER_TIMEOUT`

For additional information on how to customize the extensible SDK's
configuration, see the
":ref:`sdk-manual/appendix-customizing:configuring the extensible sdk`"
section in the Yocto Project Application Development and the
Extensible Software Development Kit (eSDK) manual.
