When inheriting the :ref:`ref-classes-features_check` class, this variable
identifies image features that must exist in the current
configuration in order for the :term:`OpenEmbedded Build System` to build
the recipe. In other words, if the :term:`REQUIRED_IMAGE_FEATURES` variable
lists a feature that does not appear in :term:`IMAGE_FEATURES` within the
current configuration, then the recipe will be skipped, and if the build
system attempts to build the recipe then an error will be triggered.

Compared to other ``REQUIRED_*_FEATURES`` variables, the
:term:`REQUIRED_IMAGE_FEATURES` varible only targets image recipes, as the
:term:`IMAGE_FEATURES` variable is handled by the :ref:`ref-classes-core-image`
class). However, the :term:`REQUIRED_IMAGE_FEATURES` varible can also be
set from a :term:`Configuration File`, such as a distro
configuration file, if the list of required image features should apply to
all images using this :term:`DISTRO`.
