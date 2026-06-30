Removes all output files and shared state
(:ref:`sstate <overview-manual/concepts:shared state cache>`) cache for a
target. Essentially, the :term:`do_cleansstate` task is identical to the
:term:`do_clean` task with the added removal of
shared state (:ref:`sstate <overview-manual/concepts:shared state cache>`)
cache.

You can run this task using BitBake as follows::

   $ bitbake -c cleansstate recipe

When you run the :term:`do_cleansstate` task, the OpenEmbedded build system
no longer uses any sstate. Consequently, building the recipe from
scratch is guaranteed.

.. note::

   Using :term:`do_cleansstate` with a shared :term:`SSTATE_DIR` is
   not recommended because it could trigger an error during the build of a
   separate BitBake instance. This is because the builds check sstate "up
   front" but download the files later, so it if is deleted in the
   meantime, it will cause an error but not a total failure as it will
   rebuild it.

   The reliable and preferred way to force a new build is to use ``bitbake
   -f`` instead.

.. note::

   The :term:`do_cleansstate` task cannot remove sstate from a remote sstate
   mirror. If you need to build a target from scratch using remote mirrors, use
   the "-f" option as follows::

      $ bitbake -f -c do_cleansstate target
