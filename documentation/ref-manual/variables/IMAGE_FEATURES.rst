The primary list of features to include in an image. Typically, you
configure this variable in an image recipe. Although you can use this
variable from your ``local.conf`` file, which is found in the
:term:`Build Directory`, best practices dictate that you do
not.

.. note::

   To enable extra features from outside the image recipe, use the
   :term:`EXTRA_IMAGE_FEATURES` variable.

For a list of image features that ships with the Yocto Project, see
the ":ref:`ref-features-image`" section.

For an example that shows how to customize your image by using this
variable, see the ":ref:`dev-manual/customizing-images:customizing images using custom \`\`image_features\`\` and \`\`extra_image_features\`\``"
section in the Yocto Project Development Tasks Manual.
