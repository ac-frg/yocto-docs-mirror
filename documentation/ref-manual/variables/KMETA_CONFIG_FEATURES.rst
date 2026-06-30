The :term:`KMETA_CONFIG_FEATURES` variable defines features enabled for the
:ref:`ref-classes-kernel-yocto` class. The following list of features are
supported:

-  ``prefer-modules``: prefer a kernel configuration to be set as ``m``
   instead of the default value ``y`` if the kernel configuration was
   defined as follows::

      CONFIG_FOO=y # OVERRIDE:$MODULE_OR_Y

The default value of this variable is an empty string.
