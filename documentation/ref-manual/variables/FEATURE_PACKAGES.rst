Defines one or more packages to include in an image when a specific
item is included in :term:`IMAGE_FEATURES`.
When setting the value, :term:`FEATURE_PACKAGES` should have the name of
the feature item as an override. Here is an example::

   FEATURE_PACKAGES_widget = "package1 package2"

In this example, if "widget" were added to :term:`IMAGE_FEATURES`,
package1 and package2 would be included in the image.

.. note::

   Packages installed by features defined through :term:`FEATURE_PACKAGES`
   are often package groups. While similarly named, you should not
   confuse the :term:`FEATURE_PACKAGES` variable with package groups, which
   are discussed elsewhere in the documentation.
