When inheriting the :ref:`ref-classes-overlayfs` class,
provides the ability to disable QA checks for particular overlayfs
mounts. For example::

   OVERLAYFS_QA_SKIP[data] = "mount-configured"

.. note::

   Although the :ref:`ref-classes-overlayfs` class is
   inherited by individual recipes, :term:`OVERLAYFS_QA_SKIP`
   should be set in your machine configuration.
