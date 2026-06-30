Specifies the command to create the image file for a specific image
type, which corresponds to the value set in
:term:`IMAGE_FSTYPES`, (e.g. ``ext3``,
``btrfs``, and so forth). When setting this variable, you should use
an override for the associated type. Here is an example::

   IMAGE_CMD:jffs2 = "mkfs.jffs2 --root=${IMAGE_ROOTFS} --faketime \
       --output=${IMGDEPLOYDIR}/${IMAGE_NAME}${IMAGE_NAME_SUFFIX}.jffs2 \
       ${EXTRA_IMAGECMD}"

You typically do not need to set this variable unless you are adding
support for a new image type. For more examples on how to set this
variable, see the :ref:`ref-classes-image_types`
class file, which is ``meta/classes-recipe/image_types.bbclass``.
