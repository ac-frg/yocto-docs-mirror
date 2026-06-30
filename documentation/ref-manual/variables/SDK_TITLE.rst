The title to be printed when running the SDK installer. By default,
this title is based on the :term:`DISTRO_NAME` or
:term:`DISTRO` variable and is set in the
:ref:`populate_sdk_base <ref-classes-populate-sdk-*>` class as
follows::

   SDK_TITLE ??= "${@d.getVar('DISTRO_NAME') or d.getVar('DISTRO')} SDK"

For the :term:`poky` reference distribution,
:term:`SDK_TITLE` is set to "Poky (Yocto Project Reference Distro)".

For information on how to change this default title, see the
":ref:`sdk-manual/appendix-customizing:changing the extensible sdk installer title`"
section in the Yocto Project Application Development and the
Extensible Software Development Kit (eSDK) manual.
