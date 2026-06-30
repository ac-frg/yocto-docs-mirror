If set to "1" along with the
:term:`COPY_LIC_MANIFEST` variable, the
OpenEmbedded build system copies into the image the license files,
which are located in ``/usr/share/common-licenses``, for each
package. The license files are placed in directories within the image
itself during build time.

.. note::

   The :term:`COPY_LIC_DIRS` does not offer a path for adding licenses for
   newly installed packages to an image, which might be most suitable for
   read-only filesystems that cannot be upgraded. See the
   :term:`LICENSE_CREATE_PACKAGE` variable for additional information.
   You can also reference the ":ref:`dev-manual/licenses:providing license text`"
   section in the Yocto Project Development Tasks Manual for
   information on providing license text.
