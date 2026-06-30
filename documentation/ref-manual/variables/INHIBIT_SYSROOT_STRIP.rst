If set to "1", causes the build to not strip binaries in the
resulting sysroot.

By default, the OpenEmbedded build system strips binaries in the
resulting sysroot. When you specifically set the
:term:`INHIBIT_SYSROOT_STRIP` variable to "1" in your recipe, you inhibit
this stripping.

If you want to use this variable, include the :ref:`ref-classes-staging`
class. This class uses a ``sys_strip()`` function to test for the variable
and acts accordingly.

.. note::

   Use of the :term:`INHIBIT_SYSROOT_STRIP` variable occurs in rare and
   special circumstances. For example, suppose you are building
   bare-metal firmware by using an external GCC toolchain. Furthermore,
   even if the toolchain's binaries are strippable, there are other files
   needed for the build that are not strippable.
