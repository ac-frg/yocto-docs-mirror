A list of variables allowed through from the OpenEmbedded build
system configuration into the extensible SDK configuration. By
default, the list of variables is empty and is set in the
:ref:`populate-sdk-ext <ref-classes-populate-sdk-*>` class.

This list overrides the variables specified using the
:term:`ESDK_LOCALCONF_REMOVE` variable as well as
other variables automatically added due to the "/" character
being found at the start of the
value, which is usually indicative of being a path and thus might not
be valid on the system where the SDK is installed.

For additional information on how to customize the extensible SDK's
configuration, see the
":ref:`sdk-manual/appendix-customizing:configuring the extensible sdk`"
section in the Yocto Project Application Development and the
Extensible Software Development Kit (eSDK) manual.
