A list of classes to globally inherit. These classes are used by the
OpenEmbedded build system to enable extra features.

Classes inherited using :term:`USER_CLASSES` must be located in the
``classes-global/`` or ``classes/`` subdirectories.

The default list is set in your ``local.conf`` file::

   USER_CLASSES ?= "buildstats"

For more information, see
``conf/templates/default/local.conf.sample`` in
:yocto_git:`meta-poky <meta-yocto/tree/meta-poky>`.
