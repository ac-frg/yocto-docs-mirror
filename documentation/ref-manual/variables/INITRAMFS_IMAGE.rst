Specifies the :term:`PROVIDES` name of an image
recipe that is used to build an initial RAM filesystem (:term:`Initramfs`)
image. In other words, the :term:`INITRAMFS_IMAGE` variable causes an
additional recipe to be built as a dependency to whatever root
filesystem recipe you might be using (e.g. ``core-image-sato``). The
:term:`Initramfs` image recipe you provide should set
:term:`IMAGE_FSTYPES` to
:term:`INITRAMFS_FSTYPES`.

An :term:`Initramfs` image provides a temporary root filesystem used for
early system initialization (e.g. loading of modules needed to locate
and mount the "real" root filesystem).

.. note::

   See the ``meta/recipes-core/images/core-image-minimal-initramfs.bb``
   recipe in :term:`OpenEmbedded-Core (OE-Core)`
   for an example :term:`Initramfs` recipe. To select this sample recipe as
   the one built to provide the :term:`Initramfs` image, set :term:`INITRAMFS_IMAGE`
   to "core-image-minimal-initramfs".

You can also find more information by referencing the
``conf/templates/default/local.conf.sample.extended``
configuration file in :yocto_git:`meta-poky <meta-yocto/tree/meta-poky>`, the :ref:`ref-classes-image`
class, and the :ref:`ref-classes-kernel` class to see how to use the
:term:`INITRAMFS_IMAGE` variable.

If :term:`INITRAMFS_IMAGE` is empty, which is the default, then no
:term:`Initramfs` image is built.

For more information, you can also see the
:term:`INITRAMFS_IMAGE_BUNDLE`
variable, which allows the generated image to be bundled inside the
kernel image. Additionally, for information on creating an :term:`Initramfs`
image, see the ":ref:`dev-manual/building:building an initial ram filesystem (Initramfs) image`" section
in the Yocto Project Development Tasks Manual.
