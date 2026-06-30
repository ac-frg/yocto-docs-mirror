Writes output files that are to be deployed to
``${``\ :term:`DEPLOY_DIR_IMAGE`\ ``}``. The
task runs with the current working directory set to
``${``\ :term:`B`\ ``}``.

Recipes implementing this task should inherit the
:ref:`ref-classes-deploy` class and should write the output
to ``${``\ :term:`DEPLOYDIR`\ ``}``, which is not to be
confused with ``${``\ :term:`DEPLOY_DIR`\ ``}``. The :ref:`ref-classes-deploy` class sets up
:term:`do_deploy` as a shared state (sstate) task that can be accelerated
through sstate use. The sstate mechanism takes care of copying the
output from ``${DEPLOYDIR}`` to ``${DEPLOY_DIR_IMAGE}``.

.. note::

   Do not write the output directly to ``${DEPLOY_DIR_IMAGE}``, as this causes
   the sstate mechanism to malfunction.

The :term:`do_deploy` task is not added as a task by default and
consequently needs to be added manually. If you want the task to run
after :term:`do_compile`, you can add it by doing
the following::

      addtask deploy after do_compile

Adding :term:`do_deploy` after other tasks works the same way.

.. note::

   You do not need to add ``before do_build`` to the ``addtask`` command
   (though it is harmless), because the :ref:`ref-classes-base` class contains the following::

           do_build[recrdeptask] += "do_deploy"


   See the ":ref:`bitbake-user-manual/bitbake-user-manual-execution:dependencies`"
   section in the BitBake User Manual for more information.

If the :term:`do_deploy` task re-executes, any previous output is removed
(i.e. "cleaned").
