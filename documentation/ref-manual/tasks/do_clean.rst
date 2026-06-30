Removes all output files for a target from the
:term:`do_unpack` task forward (i.e. :term:`do_unpack`,
:term:`do_configure`,
:term:`do_compile`,
:term:`do_install`, and
:term:`do_package`).

You can run this task using BitBake as follows::

   $ bitbake -c clean recipe

Running this task does not remove the
:ref:`sstate <overview-manual/concepts:shared state cache>` cache files.
Consequently, if no changes have been made and the recipe is rebuilt
after cleaning, output files are simply restored from the sstate cache.
If you want to remove the sstate cache files for the recipe, you need to
use the :term:`do_cleansstate` task instead
(i.e. ``bitbake -c cleansstate`` recipe).
