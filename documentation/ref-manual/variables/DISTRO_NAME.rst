The long name of the distribution. For information on the short name
of the distribution, see the :term:`DISTRO` variable.

The :term:`DISTRO_NAME` variable corresponds to a distribution
configuration file whose root name is the same as the variable's
argument and whose filename extension is ``.conf``. For example, the
distribution configuration file for the Poky distribution is named
``poky.conf`` and resides in the ``meta-poky/conf/distro`` directory
of :yocto_git:`meta-poky </meta-yocto/tree/meta-poky>`.

Within that ``poky.conf`` file, the :term:`DISTRO_NAME` variable is set
as follows::

   DISTRO_NAME = "Poky (Yocto Project Reference Distro)"

Distribution configuration files are located in a ``conf/distro``
directory within the :term:`Metadata` that contains the
distribution configuration.

.. note::

   If the :term:`DISTRO_NAME` variable is blank, a set of default
   configurations are used, which are specified within
   ``meta/conf/distro/defaultsetup.conf`` also in :term:`OpenEmbedded-Core
   (OE-Core)`.
