The revision of the recipe. The default value for this variable is
"r0". Subsequent revisions of the recipe conventionally have the
values "r1", "r2", and so forth. When :term:`PV` increases,
:term:`PR` is conventionally reset to "r0".

.. note::

   The OpenEmbedded build system does not need the aid of :term:`PR`
   to know when to rebuild a recipe. The build system uses the task
   :ref:`input checksums <overview-manual/concepts:checksums (signatures)>` along with the
   :ref:`stamp <structure-build-tmp-stamps>` and
   :ref:`overview-manual/concepts:shared state cache`
   mechanisms.

The :term:`PR` variable primarily becomes significant when a package
manager dynamically installs packages on an already built image. In
this case, :term:`PR`, which is the default value of
:term:`PKGR`, helps the package manager distinguish which
package is the most recent one in cases where many packages have the
same :term:`PV` (i.e. :term:`PKGV`). A component having many packages with
the same :term:`PV` usually means that the packages all install the same
upstream version, but with later (:term:`PR`) version packages including
packaging fixes.

.. note::

   :term:`PR` does not need to be increased for changes that do not change the
   package contents or metadata.

Because manually managing :term:`PR` can be cumbersome and error-prone,
an automated solution exists. See the
":ref:`dev-manual/packages:working with a pr service`" section
in the Yocto Project Development Tasks Manual for more information.
