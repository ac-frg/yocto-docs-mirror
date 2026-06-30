.. SPDX-License-Identifier: CC-BY-SA-2.0-UK

*****
Tasks
*****

Tasks are units of execution for BitBake. Recipes (``.bb`` files) use
tasks to complete configuring, compiling, and packaging software. This
chapter provides a reference of the tasks defined in the OpenEmbedded
build system.

To see the tasks defined (in alphabetical order) for a given recipe,
you can run:

.. code-block:: console

   $ bitbake -c listtasks recipename
   do_build                              Default task for a recipe - depends on all other normal tasks required to 'build' a recipe
   do_checkuri                           Validates the SRC_URI value
   do_clean                              Removes all output files for a target
   do_cleanall                           Removes all output files, shared state cache, and downloaded source files for a target
   do_cleansstate                        Removes all output files and shared state cache for a target
   do_compile                            Compiles the source in the compilation directory
   ...

In addition, once a recipe has been built, you can examine the
resulting task information in that recipe's ``${WORKDIR}/temp/``
directory, which will consist of the following:

-  for each task, a ``run`` file that represents the code that
   was executed for that task

-  for each task, a corresponding ``log`` file showing the result of
   task execution

-  a single ``log.task_order`` file showing the execution order
   of all tasks for that recipe

Normal Recipe Build Tasks
=========================

The following sections describe normal tasks associated with building a
recipe. For more information on tasks and dependencies, see the
":ref:`bitbake-user-manual/bitbake-user-manual-metadata:tasks`" and
":ref:`bitbake-user-manual/bitbake-user-manual-execution:dependencies`" sections in the
BitBake User Manual.

.. glossary::
   :sorted:

   :term:`do_build`
      .. include:: tasks/do_build.rst

   :term:`do_compile`
      .. include:: tasks/do_compile.rst

   :term:`do_compile_ptest_base`
      .. include:: tasks/do_compile_ptest_base.rst

   :term:`do_configure`
      .. include:: tasks/do_configure.rst

   :term:`do_configure_ptest_base`
      .. include:: tasks/do_configure_ptest_base.rst

   :term:`do_deploy`
      .. include:: tasks/do_deploy.rst

   :term:`do_fetch`
      .. include:: tasks/do_fetch.rst

   :term:`do_image`
      .. include:: tasks/do_image.rst

   :term:`do_image_complete`
      .. include:: tasks/do_image_complete.rst

   :term:`do_install`
      .. include:: tasks/do_install.rst

   :term:`do_install_ptest_base`
      .. include:: tasks/do_install_ptest_base.rst

   :term:`do_package`
      .. include:: tasks/do_package.rst

   :term:`do_package_qa`
      .. include:: tasks/do_package_qa.rst

   :term:`do_package_write_deb`
      .. include:: tasks/do_package_write_deb.rst

   :term:`do_package_write_ipk`
      .. include:: tasks/do_package_write_ipk.rst

   :term:`do_package_write_rpm`
      .. include:: tasks/do_package_write_rpm.rst

   :term:`do_packagedata`
      .. include:: tasks/do_packagedata.rst

   :term:`do_patch`
      .. include:: tasks/do_patch.rst

   :term:`do_populate_lic`
      .. include:: tasks/do_populate_lic.rst

   :term:`do_populate_sdk`
      .. include:: tasks/do_populate_sdk.rst

   :term:`do_populate_sdk_ext`
      .. include:: tasks/do_populate_sdk_ext.rst

   :term:`do_populate_sysroot`
      .. include:: tasks/do_populate_sysroot.rst

   :term:`do_prepare_recipe_sysroot`
      .. include:: tasks/do_prepare_recipe_sysroot.rst

   :term:`do_recipe_qa`
      .. include:: tasks/do_recipe_qa.rst

   :term:`do_rm_work`
      .. include:: tasks/do_rm_work.rst

   :term:`do_unpack`
      .. include:: tasks/do_unpack.rst

Manually Called Tasks
=====================

These tasks are typically manually triggered (e.g. by using the
``bitbake -c`` command-line option) because they are not normally
part of any standard build workflow. As an example, consider the
``listtasks`` task, which displays the tasks defined for a given
recipe and would be invoked with:

.. code-block:: console

   $ bitbake -c listtasks recipename

A typical definition of a manually-called task would look like::

   addtask listtasks
   do_listtasks[nostamp] = "1"
   python do_listtasks() {
      ... definition of task ...
   }

which defines that function as a task without building it into any
task dependency chain, as well as setting the ``[nostamp]`` flag to
ensure that it is run every time it is invoked.

.. glossary::
   :sorted:

   :term:`do_checkuri`
      .. include:: tasks/do_checkuri.rst

   :term:`do_clean`
      .. include:: tasks/do_clean.rst

   :term:`do_cleanall`
      .. include:: tasks/do_cleanall.rst

   :term:`do_cleansstate`
      .. include:: tasks/do_cleansstate.rst

   :term:`do_pydevshell`
      .. include:: tasks/do_pydevshell.rst

   :term:`do_devshell`
      .. include:: tasks/do_devshell.rst

   :term:`do_list_image_features`
      .. include:: tasks/do_list_image_features.rst

   :term:`do_listtasks`
      .. include:: tasks/do_listtasks.rst

   :term:`do_package_index`
      .. include:: tasks/do_package_index.rst

Image-Related Tasks
===================

The following tasks are applicable to image recipes.

.. glossary::
   :sorted:

   :term:`do_bootimg`
      .. include:: tasks/do_bootimg.rst

   :term:`do_bundle_initramfs`
      .. include:: tasks/do_bundle_initramfs.rst

   :term:`do_rootfs`
      .. include:: tasks/do_rootfs.rst

   :term:`do_testimage`
      .. include:: tasks/do_testimage.rst

   :term:`do_testimage_auto`
      .. include:: tasks/do_testimage_auto.rst

Kernel-Related Tasks
====================

The following tasks are applicable to kernel recipes. Some of these
tasks (e.g. the :term:`do_menuconfig` task) are
also applicable to recipes that use Linux kernel style configuration
such as the BusyBox recipe.

.. glossary::
   :sorted:

   :term:`do_compile_kernelmodules`
      .. include:: tasks/do_compile_kernelmodules.rst

   :term:`do_diffconfig`
      .. include:: tasks/do_diffconfig.rst

   :term:`do_kernel_checkout`
      .. include:: tasks/do_kernel_checkout.rst

   :term:`do_kernel_configcheck`
      .. include:: tasks/do_kernel_configcheck.rst

   :term:`do_kernel_configme`
      .. include:: tasks/do_kernel_configme.rst

   :term:`do_kernel_metadata`
      .. include:: tasks/do_kernel_metadata.rst

   :term:`do_menuconfig`
      .. include:: tasks/do_menuconfig.rst

   :term:`do_savedefconfig`
      .. include:: tasks/do_savedefconfig.rst

   :term:`do_shared_workdir`
      .. include:: tasks/do_shared_workdir.rst

   :term:`do_sizecheck`
      .. include:: tasks/do_sizecheck.rst

   :term:`do_strip`
      .. include:: tasks/do_strip.rst

   :term:`do_validate_branches`
      .. include:: tasks/do_validate_branches.rst

