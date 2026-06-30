Indicates the deploy directory used by :term:`do_bundle_initramfs`
where the :term:`INITRAMFS_IMAGE` will be fetched from. This variable is
set by default to ``${DEPLOY_DIR_IMAGE}`` in the
:ref:`ref-classes-kernel` class and it's only meant to be changed when
building an :term:`Initramfs` image from a separate multiconfig via
:term:`INITRAMFS_MULTICONFIG`.
