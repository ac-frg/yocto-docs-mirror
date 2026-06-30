The default installation directory for the Extensible SDK. By
default, this directory is based on the :term:`DISTRO`
variable and is set in the
:ref:`populate_sdk_base <ref-classes-populate-sdk-*>` class as
follows::

   SDKEXTPATH ??= "~/${@d.getVar('DISTRO')}_sdk"

For the
:term:`Poky` reference distro, the :term:`SDKEXTPATH` is set to "poky_sdk".

For information on how to change this default directory, see the
":ref:`sdk-manual/appendix-customizing:changing the default sdk installation directory`"
section in the Yocto Project Application Development and the
Extensible Software Development Kit (eSDK) manual.
