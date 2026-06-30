The manifest file for the target part of the SDK. This file lists all
the installed packages that make up the target part of the SDK. The
file contains package information on a line-per-package basis as
follows::

   packagename packagearch version

The :ref:`populate_sdk_base <ref-classes-populate-sdk-*>` class
defines the manifest file as follows::

   SDK_TARGET_MANIFEST = "${SDK_DEPLOY}/${TOOLCHAIN_OUTPUTNAME}.target.manifest"

The location is derived using the :term:`SDK_DEPLOY` and
:term:`TOOLCHAIN_OUTPUTNAME` variables.
