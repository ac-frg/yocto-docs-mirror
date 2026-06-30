The version of the package(s) built by the recipe. By default,
:term:`PKGV` is set to :term:`PV`.

If :term:`PV` contains the ``+`` sign, source control information will be
included in :term:`PKGV` later in the packaging phase. For more
information, see the :doc:`/dev-manual/external-scm` section of the Yocto
Project Development Tasks Manual.

.. warning::

   Since source control information is included in a late stage by the
   :ref:`ref-classes-package` class, it cannot be seen from the BitBake
   environment with ``bitbake -e`` or ``bitbake-getvar``. Instead, after
   the package is built, the version information can be retrieved with
   ``oe-pkgdata-util package-info <package name>``. See the
   :ref:`dev-manual/debugging:Viewing Package Information with
   ``oe-pkgdata-util``` section of the Yocto Project Development Tasks
   Manual for more information on ``oe-pkgdata-util``.
