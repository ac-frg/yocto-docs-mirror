A list of classes to remove from the :term:`INHERIT`
value globally within the extensible SDK configuration. The
:ref:`populate-sdk-ext <ref-classes-populate-sdk-*>` class sets the
default value::

   ESDK_CLASS_INHERIT_DISABLE ?= "buildhistory"

Some classes are not generally applicable within the extensible SDK
context. You can use this variable to disable those classes.

For additional information on how to customize the extensible SDK's
configuration, see the
":ref:`sdk-manual/appendix-customizing:configuring the extensible sdk`"
section in the Yocto Project Application Development and the
Extensible Software Development Kit (eSDK) manual.
