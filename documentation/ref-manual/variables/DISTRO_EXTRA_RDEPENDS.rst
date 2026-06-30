Specifies a list of distro-specific packages to add to all images.
This variable takes effect through ``packagegroup-base`` so the
variable only really applies to the more full-featured images that
include ``packagegroup-base``. You can use this variable to keep
distro policy out of generic images. As with all other distro
variables, you set this variable in the distro ``.conf`` file.
