Lists classes that will be inherited at the distribution level. It is
unlikely that you want to edit this variable.

Classes specified in :term:`INHERIT_DISTRO` must be located in the
``classes-global/`` or ``classes/`` subdirectories.

The default value of the variable is set as follows in the
``meta/conf/distro/defaultsetup.conf`` file::

   INHERIT_DISTRO ?= "debian devshell sstate license remove-libtool create-spdx"
