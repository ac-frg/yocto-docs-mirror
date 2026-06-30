Copies files that are to be packaged into the holding area
``${``\ :term:`D`\ ``}``. This task runs with the current
working directory set to ``${``\ :term:`B`\ ``}``, which is the
compilation directory. The :term:`do_install` task, as well as other tasks
that either directly or indirectly depend on the installed files (e.g.
:term:`do_package`, :term:`do_package_write_* <do_package_write_deb>`, and
:term:`do_rootfs`), run under
:ref:`fakeroot <overview-manual/concepts:fakeroot and pseudo>`.

.. note::

   When installing files, be careful not to set the owner and group IDs
   of the installed files to unintended values. Some methods of copying
   files, notably when using the recursive ``cp`` command, can preserve
   the UID and/or GID of the original file, which is usually not what
   you want. The ``host-user-contaminated`` QA check checks for files
   that probably have the wrong ownership.

   Safe methods for installing files include the following:

   -  The ``install`` utility. This utility is the preferred method.

   -  The ``cp`` command with the ``--no-preserve=ownership`` option.

   -  The ``tar`` command with the ``--no-same-owner`` option. See the
      ``bin_package.bbclass`` file in the ``meta/classes-recipe``
      subdirectory of :term:`OpenEmbedded-Core (OE-Core)` for an example.
