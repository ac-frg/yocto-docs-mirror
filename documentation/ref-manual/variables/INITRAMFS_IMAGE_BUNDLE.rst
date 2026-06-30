Controls whether or not the image recipe specified by
:term:`INITRAMFS_IMAGE` is run through an
extra pass
(:term:`do_bundle_initramfs`) during
kernel compilation in order to build a single binary that contains
both the kernel image and the initial RAM filesystem (:term:`Initramfs`)
image. This makes use of the
:term:`CONFIG_INITRAMFS_SOURCE` kernel
feature.

.. note::

   Bundling the :term:`Initramfs` with the kernel conflates the code in the
   :term:`Initramfs` with the GPLv2 licensed Linux kernel binary. Thus only GPLv2
   compatible software may be part of a bundled :term:`Initramfs`.

.. note::

   Using an extra compilation pass to bundle the :term:`Initramfs` avoids a
   circular dependency between the kernel recipe and the :term:`Initramfs`
   recipe should the :term:`Initramfs` include kernel modules. Should that be
   the case, the :term:`Initramfs` recipe depends on the kernel for the
   kernel modules, and the kernel depends on the :term:`Initramfs` recipe
   since the :term:`Initramfs` is bundled inside the kernel image.

The combined binary is deposited into the ``tmp/deploy`` directory,
which is part of the :term:`Build Directory`.

Setting the variable to "1" in a configuration file causes the
OpenEmbedded build system to generate a kernel image with the
:term:`Initramfs` specified in :term:`INITRAMFS_IMAGE` bundled within::

   INITRAMFS_IMAGE_BUNDLE = "1"

By default, the :ref:`ref-classes-kernel` class sets this variable to a
null string as follows::

   INITRAMFS_IMAGE_BUNDLE ?= ""

.. note::

   You must set the :term:`INITRAMFS_IMAGE_BUNDLE` variable in a
   configuration file. You cannot set the variable in a recipe file.

See the
:oecore_path:`local.conf.sample.extended <meta/conf/templates/default/local.conf.sample.extended>`
file for additional information. Also, for information on creating an
:term:`Initramfs`, see the ":ref:`dev-manual/building:building an initial ram filesystem (Initramfs) image`" section
in the Yocto Project Development Tasks Manual.
