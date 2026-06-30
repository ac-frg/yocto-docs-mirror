This value needs to stay in sync with :term:`IMAGE_LINK_NAME`, but with
:term:`INITRAMFS_IMAGE` instead of :term:`IMAGE_BASENAME`. The default value
is set as follows:

   INITRAMFS_IMAGE_NAME ?= "${@['${INITRAMFS_IMAGE}${IMAGE_MACHINE_SUFFIX}', ''][d.getVar('INITRAMFS_IMAGE') == '']}"

That is, if :term:`INITRAMFS_IMAGE` is set, the value of
:term:`INITRAMFS_IMAGE_NAME` will be set based upon
:term:`INITRAMFS_IMAGE` and :term:`IMAGE_MACHINE_SUFFIX`.
