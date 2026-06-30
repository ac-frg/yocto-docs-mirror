Triggers the OpenEmbedded build system's shared libraries resolver to
exclude an entire package when scanning for shared libraries.

.. note::

   The shared libraries resolver's functionality results in part from
   the internal function ``package_do_shlibs``, which is part of the
   :term:`do_package` task. You should be aware that the shared
   libraries resolver might implicitly define some dependencies between
   packages.

The :term:`EXCLUDE_FROM_SHLIBS` variable is similar to the
:term:`PRIVATE_LIBS` variable, which excludes a
package's particular libraries only and not the whole package.

Use the :term:`EXCLUDE_FROM_SHLIBS` variable by setting it to "1" for a
particular package::

   EXCLUDE_FROM_SHLIBS = "1"
