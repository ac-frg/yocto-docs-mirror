Removes all output files, shared state
(:ref:`sstate <overview-manual/concepts:shared state cache>`) cache, and
downloaded source files for a target (i.e. the contents of
:term:`DL_DIR`). Essentially, the :term:`do_cleanall` task is
identical to the :term:`do_cleansstate` task
with the added removal of downloaded source files.

You can run this task using BitBake as follows::

   $ bitbake -c cleanall recipe

You should never use the :term:`do_cleanall` task in a normal
scenario. If you want to start fresh with the :term:`do_fetch` task,
use instead::

  $ bitbake -f -c fetch recipe

.. note::

   The reason to prefer ``bitbake -f -c fetch`` is that the
   :term:`do_cleanall` task would break in some cases, such as::

      $ bitbake -c fetch    recipe
      $ bitbake -c cleanall recipe-native
      $ bitbake -c unpack   recipe

   because after step 1 there is a stamp file for the
   :term:`do_fetch` task of ``recipe``, and it won't be removed at
   step 2 because step 2 uses a different work directory. So the unpack task
   at step 3 will try to extract the downloaded archive and fail as it has
   been deleted in step 2.

   Note that this also applies to BitBake from concurrent processes when a
   shared download directory (:term:`DL_DIR`) is setup.
