The destination directory. The location in the :term:`Build Directory`
where components are installed by the
:term:`do_install` task. This location defaults
to::

   ${WORKDIR}/image

.. note::

   Tasks that read from or write to this directory should run under
   :ref:`fakeroot <overview-manual/concepts:fakeroot and pseudo>`.
