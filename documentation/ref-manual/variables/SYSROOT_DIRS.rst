Directories that are staged into the sysroot by the
:term:`do_populate_sysroot` task. By
default, the following directories are staged::

   SYSROOT_DIRS = " \
       ${includedir} \
       ${libdir} \
       ${base_libdir} \
       ${nonarch_base_libdir} \
       ${datadir} \
       /sysroot-only \
       "

Consider the following example in which you need to manipulate this variable.
Assume you have a recipe ``A`` that provides a shared library ``.so.*`` that is
installed into a custom folder other than "``${libdir}``"
or "``${base_libdir}``", let's say "``/opt/lib``".

.. note::

   This is not a recommended way to deal with shared libraries, but this
   is just to show the usefulness of setting :term:`SYSROOT_DIRS`.

When a recipe ``B`` :term:`DEPENDS` on ``A``, it means what is in
:term:`SYSROOT_DIRS` will be copied from :term:`D` of the recipe ``A``
into ``B``'s :term:`SYSROOT_DESTDIR` that is "``${WORKDIR}/sysroot-destdir``".

Now, since ``/opt/lib`` is not in :term:`SYSROOT_DIRS`, it will never be copied to
``A``'s :term:`RECIPE_SYSROOT`, which is "``${WORKDIR}/recipe-sysroot``". So,
the linking process will fail.

To fix this, you need to add ``/opt/lib`` to :term:`SYSROOT_DIRS`::

   SYSROOT_DIRS:append = " /opt/lib"

.. note::
   Even after setting ``/opt/lib`` to :term:`SYSROOT_DIRS`, the linking process will still fail
   because the linker does not know that location, since :term:`TARGET_LDFLAGS`
   doesn't contain it (if your recipe is for the target). Therefore, so you should add::

      TARGET_LDFLAGS:append = " -L${RECIPE_SYSROOT}/opt/lib"
