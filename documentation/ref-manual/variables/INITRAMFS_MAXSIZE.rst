Defines the maximum allowed size of the :term:`Initramfs` image in Kbytes.
The build will fail if the :term:`Initramfs` image size exceeds this value.

The :term:`Initramfs` image size undergoes several calculation steps before
being compared to :term:`INITRAMFS_MAXSIZE`.
These steps are the same as those used for :term:`IMAGE_ROOTFS_MAXSIZE`
and are described in detail in that entry.

Thus, :term:`INITRAMFS_MAXSIZE` is compared with the result of the calculations
and is independent of the final image type (e.g. compressed).
A default value for :term:`INITRAMFS_MAXSIZE` is set in
:oe_git:`meta/conf/bitbake.conf </openembedded-core/tree/meta/conf/bitbake.conf>`.
