This variable defines the name used for the toolchain output. The
:ref:`populate_sdk_base <ref-classes-populate-sdk-*>` class sets
the :term:`TOOLCHAIN_OUTPUTNAME` variable as follows::

   TOOLCHAIN_OUTPUTNAME ?= "${SDK_NAME}-toolchain-${SDK_VERSION}"

See
the :term:`SDK_NAME` and
:term:`SDK_VERSION` variables for additional
information.
