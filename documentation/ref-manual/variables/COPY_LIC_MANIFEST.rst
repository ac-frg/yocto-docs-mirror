If set to "1", the OpenEmbedded build system copies the license
manifest for the image to
``/usr/share/common-licenses/license.manifest`` within the image
itself during build time.

.. note::

   The :term:`COPY_LIC_MANIFEST` does not offer a path for adding licenses for
   newly installed packages to an image, which might be most suitable for
   read-only filesystems that cannot be upgraded. See the
   :term:`LICENSE_CREATE_PACKAGE` variable for additional information.
   You can also reference the ":ref:`dev-manual/licenses:providing license text`"
   section in the Yocto Project Development Tasks Manual for
   information on providing license text.
