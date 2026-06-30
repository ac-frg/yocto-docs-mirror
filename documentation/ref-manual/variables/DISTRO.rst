The short name of the distribution. For information on the long name
of the distribution, see the :term:`DISTRO_NAME`
variable.

The :term:`DISTRO` variable corresponds to a distribution configuration
file whose root name is the same as the variable's argument and whose
filename extension is ``.conf``. For example, the distribution
configuration file for the Poky distribution is named ``poky.conf``
and resides in the ``meta-poky/conf/distro`` directory of
:yocto_git:`meta-poky </meta-yocto/tree/meta-poky>`.

Within that ``poky.conf`` file, the :term:`DISTRO` variable is set as
follows::

   DISTRO = "poky"

Distribution configuration files are located in a ``conf/distro``
directory within the :term:`Metadata` that contains the
distribution configuration. The value for :term:`DISTRO` must not contain
spaces, and is typically all lower-case.

.. note::

   If the :term:`DISTRO` variable is blank, a set of default configurations
   are used, which are specified within
   ``meta/conf/distro/defaultsetup.conf`` also in :term:`OpenEmbedded-Core
   (OE-Core)`.
