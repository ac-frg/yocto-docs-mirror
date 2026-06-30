Points to the general area that the OpenEmbedded build system uses to
place images, packages, SDKs, and other output files that are ready
to be used outside of the build system. By default, this directory
resides within the :term:`Build Directory` as ``${TMPDIR}/deploy``.

For more information on the structure of the Build Directory, see
":ref:`ref-manual/structure:the build directory --- ``build/```" section.
For more detail on the contents of the ``deploy`` directory, see the
":ref:`overview-manual/concepts:images`",
":ref:`overview-manual/concepts:package feeds`", and
":ref:`overview-manual/concepts:application development sdk`" sections all in the
Yocto Project Overview and Concepts Manual.

.. warning::

   Do not confuse this variable with the similarly-named
   :term:`DEPLOYDIR` variable.
