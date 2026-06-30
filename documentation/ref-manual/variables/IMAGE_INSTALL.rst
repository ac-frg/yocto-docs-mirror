Used by recipes to specify the packages to install into an image
through the :ref:`ref-classes-image` class. Use the
:term:`IMAGE_INSTALL` variable with care to avoid ordering issues.

Image recipes set :term:`IMAGE_INSTALL` to specify the packages to
install into an image through :ref:`ref-classes-image`. Additionally,
there are "helper" classes such as the :ref:`ref-classes-core-image`
class which can take lists used with :term:`IMAGE_FEATURES` and turn
them into auto-generated entries in :term:`IMAGE_INSTALL` in addition
to its default contents.

When you use this variable, it is best to use it as follows::

   IMAGE_INSTALL:append = " package-name"

Be sure to include the space
between the quotation character and the start of the package name or
names.

.. note::

   -  When working with a
      :ref:`core-image-minimal-initramfs <ref-manual/images:images>`
      image, do not use the :term:`IMAGE_INSTALL` variable to specify
      packages for installation. Instead, use the
      :term:`PACKAGE_INSTALL` variable, which
      allows the initial RAM filesystem (:term:`Initramfs`) recipe to use a
      fixed set of packages and not be affected by :term:`IMAGE_INSTALL`.
      For information on creating an :term:`Initramfs`, see the
      ":ref:`dev-manual/building:building an initial ram filesystem (Initramfs) image`"
      section in the Yocto Project Development Tasks Manual.

   -  Using :term:`IMAGE_INSTALL` with the
      :ref:`+= <bitbake-user-manual/bitbake-user-manual-metadata:appending (+=) and prepending (=+) with spaces>`
      BitBake operator within the ``/conf/local.conf`` file or from
      within an image recipe is not recommended. Use of this operator in
      these ways can cause ordering issues. Since
      :ref:`ref-classes-core-image` sets :term:`IMAGE_INSTALL` to a
      default value using the
      :ref:`?= <bitbake-user-manual/bitbake-user-manual-metadata:setting a default value (?=)>`
      operator, using a ``+=`` operation against :term:`IMAGE_INSTALL`
      results in unexpected behavior when used within
      ``conf/local.conf``. Furthermore, the same operation from within an
      image recipe may or may not succeed depending on the specific
      situation. In both these cases, the behavior is contrary to how
      most users expect the ``+=`` operator to work.
