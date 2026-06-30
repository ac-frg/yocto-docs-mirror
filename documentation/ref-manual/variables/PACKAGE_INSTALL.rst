The final list of packages passed to the package manager for
installation into the image.

Because the package manager controls actual installation of all
packages, the list of packages passed using :term:`PACKAGE_INSTALL` is
not the final list of packages that are actually installed. This
variable is internal to the image construction code. Consequently, in
general, you should use the
:term:`IMAGE_INSTALL` variable to specify
packages for installation. The exception to this is when working with
the :ref:`core-image-minimal-initramfs <ref-manual/images:images>`
image. When working with an initial RAM filesystem (:term:`Initramfs`) image,
use the :term:`PACKAGE_INSTALL` variable. For information on creating an
:term:`Initramfs`, see the ":ref:`dev-manual/building:building an initial ram filesystem (Initramfs) image`" section
in the Yocto Project Development Tasks Manual.
