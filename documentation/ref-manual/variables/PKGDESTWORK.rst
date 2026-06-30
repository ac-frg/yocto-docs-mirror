Points to a temporary work area where the
:term:`do_package` task saves package metadata.
The :term:`PKGDESTWORK` location defaults to the following::

   ${WORKDIR}/pkgdata

Do not change this default.

The :term:`do_packagedata` task copies the
package metadata from :term:`PKGDESTWORK` to
:term:`PKGDATA_DIR` to make it available globally.
